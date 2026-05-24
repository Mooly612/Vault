<%*
const file = app.workspace.getActiveFile();
const content = await app.vault.read(file);
// убираем frontmatter из подсчёта
const withoutFrontmatter = content.replace(/^---[\s\S]*?---\n/, '');
const words = withoutFrontmatter.trim().split(/\s+/).filter(w => w.length > 0).length;
await app.fileManager.processFrontMatter(file, fm => { fm.words = words; });
-%>

