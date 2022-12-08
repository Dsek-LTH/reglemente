# Reglemente

Detta är reglementet för D-sektionen inom TLTH. Under "Releases" finns alla versioner av reglementet. Läs commit-meddelanden för en mer detaljerad historik.

## Användning
All text i repot ska vara skrivet på svenska.

### Efter ett sektionsmöte
* Klona repot. `git clone https://github.com/Dsek-LTH/reglemente.git`
* Om du redan klonat det, se till att du är på senaste revisionen. `git checkout master && git pull`
* Skapa en ny branch. `git checkout -b [branchnamn, tex HTM2-2019]`
* För varje motion och proposition:
    * Ändra main.tex på det sätt som krävs för den nya motionen eller propositionen.
    * Efter varje införd ändring skapa en commit med ett meddelande innehållande mötesförkortningen och ändringen. `git commit -m "[HTM2 2018] La till nya åligganden under Staben"`
    * Om en mer detaljerad beskrivning behövs bör kroppen av commitens meddelande istället användas. `git commit`
* Se till att att mötesnamn och dagens datum står på varje sida i reglementet högst upp i högra hörnet.
* Pusha upp din branch till Github. `git push -u origin [branchnamn, tex HTM2-2019]`
* Öppna en pull request på https://github.com/Dsek-LTH/reglemente/pulls för att få med dina ändringar till huvudbranchen.
* När denna godkänts skapas en ny release och PDF automatiskt.

### När du vill göra redaktionella ändringar
Redaktionella ändringar ändrar inte betydelsen av reglementet, utan ändrar enbart läsbarheten eller rättar små uppenbara fel. För att skapa en redaktionell ändring, följ instruktionerna för "Efter ett sektionsmöte" med undantag för att commit-meddelandet inte ska innehålla en mötesförkortning utan istället [Redaktionella ändringar]. `git commit -m "[Redaktionella ändringar] Fixade stavfel"`. Döp gärna branchen till något i stil med "redaktionellaandringar".

### När du vill göra ändringar till repot
Ändringar som inte påverkar reglementet direkt, så som ändringar av continuous integration eller README-filen, ska inte innehålla en mötesförkortning utan istället [Repoändringar]. `git commit -m "[Repoändringar] Uppdaterade README"`. Döp gärna branchen till något i stil med "repoandringar"

## Historik
Vid höstterminsmöte 1 2017 togs ett beslut att införa historik för sektionens styrdokument. Det togs även ett beslut att ålägga styrelsen att retroaktivt i den mån det går att införa denna historik. Detta påbörjades genom att i början i styrdokumenten fylla i en tabell med: datum, möte som tog beslutet, motion och vad som ändrades i klartext. Detta var inte hållbart i längden och Styrelsen 2019 flyttade hantering av historiken till Github. Den tidigare historiken ligger i en tidigt commit kallad "tidigare historik". De första ändringarna till styrdokumenten Github användes för var besluten från höstterminsmöte 2 2018.

## Autoformatering
Inbyggt i de flesta tex installationer finns programmet `latexindent` medföljande. Genom att köra `latexindent main.tex -w` för att se till att formateringen blir korrekt. Om du får varningar om att du saknar perl-paket när du kör `latexindent --version`, testa att köra `sudo cpan Log::LogDispatch Log::Dispatch::File YAML::Tiny File::HomeDir Log::Log4perl Unicode::GCString Getopt::Long` för att installera dessa.
