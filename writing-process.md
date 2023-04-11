# Paper Starter Kit

## References ##

- [How to Write a Paper in a Weekend](https://www.youtube.com/watch?v=UY7sVKJPTMA)
- [Skillful writing of an awful research
  paper](https://pubs.acs.org/doi/10.1021/ac2000169)
- [PhD: How to write a great research
  paper](https://www.youtube.com/watch?v=1AYxMbYZQ1Y)
- Personal experience and opinions...

## Writing Process ##

 1. Start a general outline by answering the questions.
	- Easiest to start with Lab Testing and Field Deployment. 
	- Write Introduction last!
	- Ignore questions not relevant to your project.
	- Use clear plain language statements.[^6]
	- Use jargon, acronyms, and technical terms where appropriate.[^7]
 2. Note in outline where statements need backing up.
 3. Find ways to back up those statements (still clear plain language)
    - References if already proven.[^8]
    - Further research where necessary.
    - Further experiments/demonstrations where necessary.
    - Delete where not able to back up.
    - Leave markers (@Fig:qq), (@Tbl:qq), (@Lst:qq), [@qq] where
      things still need to be done. These are easily searched for
      later.
 4. Note in outline where a figure, table, equation, or code example
    would provide greater clarity.
 5. Develop each figure, table, equation, or code example.
	- Note: no titles on figures
 6. Save outline for use as speaking notes and poster development.
 6. Write captions.
     1. Items w/ captions should stand on their own. Many people will
		scan your paper by just reading these.
     2. Captions should completely describe the image for screen readers
     3. Information in captions does not need to be repeated in body
		text, just references. For example, "Fig 1 shows the
		conceptual design"
 7. Form outline into full sentences (still clear plain language).
 8. Group sentences into paragraphs.
 9. Define jargon, acronyms, and technical terms on first use.
 10. Clean up transitions, grammar, and general language. Add any
     stylistic flourish required.
 
## Stylistic Notes ##

  * State things as plainly as a possible. 
	* As a general rule, the shortest version of a statement is the
      most clear version.
  * Use past tense when describing actions and events that happened in the past.
  * Use future tense when describing actions and events that will
    happen in the future.
  * Use present tense otherwise.
  * Use personal pronouns (I/we) when describing actions taken by the authors.
  * Use passive voice when the object being acted upon is more
    important to understanding than the subject doing the action.
      * "The system was tested at depth."
  * Use active voice when the subject taking the action is more
    important than the object being acted upon.
      * "The manipulator grasped the target."
  * DRY writing: Don't Repeat Yourself
      * NOTE: this is not always possible and some disagree with it,
        but it a good guideline rather than hard rule
      * lengthens the paper
      * adds risk of typos (correct something in one spot but not others)
	  * If information is in a figure, caption, table reference it
        rather than repeating it. 
           * ex: if you rerun code and update table information, you do
		  not want to have to rewrite parts of your paper.

## References ##

  * All figures should be referenced.
  * I prefer to reference figures as parenthesis
      * "The proposed design (@Fig:solution) was made..."
  * Others pefer (sometimes mandate) to reference in the sentence
      * "The proposed design, shown in @Fig:solution, was made..."
  * Generally use whichever produces a cleaner less wordy sentence 

  * TODO: look this up in IEEE style guide

## Citations ##

  * Do not cite a reference just to pad bibliography!
  * Read your references
  * Do not cite anything you think is poor quality.
  * Explain why you are citing
      * Comparable project?
	  * Did you use it to help with your work?
	  * Is it providing important background knowledge to understand
        your paper?
	  * Is it providing a technical reference for some piece of
        information?
  * Favor more general references
	  * Textbook > review article > journal > conference
  * I prefer to reference figures as parenthesis
      * "The thick lens model [1] was used..."
  * Others pefer (sometimes mandate) to reference in the sentence
      * "The thick lens model, described by [1], was used..."
  * Generally use whichever produces a cleaner less wordy sentence 
      * IEEE and others use the [1] style which look silly when used as word
        replacements.
      * Other journals use the Shomberg 2023 style which looks better
        in a sentence, but I still pefer parenthesis or footnote

  * TODO: look this up in IEEE style guide
  * TODO: try out different reference management styles
      * zotero
      * endnote
      * bib files
      * helm-bibtex

## Figures ##

For python figures, use matplotlib and either seaborn @Lst:pyfig1 or
[scienceplots](https://pypi.org/project/SciencePlots/1.0.2/) @Lst:pyfig2



```{.python #lst:pyfig1 caption="Set up python figures with seaborn"}
import matplotlib.pyplot as plt
import seaborn as sns
sns.set_theme(context='notebook', style='darkgrid',
	palette='deep', font='sans-serif',
	font_scale=1,color_codes=True,rc=None)
plt.rcParams.update({'figure.dpi': '200'})	
```


```{.python #lst:pyfig2 caption="Set up python figures with scienceplots"}
import scienceplots
plt.style.use(['science','nature'])
plt.rcParams.update({'figure.dpi': '200'}) 
```

  * MATLAB for charts/plots @Lst:mlfig1
      * not recommended, python is better
      * https://www.youtube.com/watch?v=sMMn0X3XKyI
  * Inkscape for diagrams
      * https://www.youtube.com/watch?v=ITpjjDETGk8
      * [ ] make a template file
      * https://tex.stackexchange.com/questions/61274/is-there-any-way-to-type-latex-code-directly-into-the-text-boxes-inkscape
      * Make a single drawings file and put margins and columns inside
          * export figures as needed
      <!-- * https://github.com/seebk/LaTeXText -->
	  * https://tex.stackexchange.com/questions/257147/how-to-use-latex-with-inkscape-mac-os-x
  * CAD renders
  * CAD line drawings
  * Photos
  * https://mentor.ieee.org/myproject/file/public/mytools/draft/stylegraph.pdf
  
```{.matlab #lst:mlfig1 caption="Function for setting up figures in matlab"}
function hfig = setup_figure(cols, rows, fsize)
arguments
    cols = 1
    rows = 1
    fsize = 10
end

hw_ratio = 9/16;


macbook_m1_16in_ppi = 226.42;
macbook_m1_16in_ext_ppi = 137.68;
asus_monitor_21in5_ppi = 102.46;

ppi = macbook_m1_16in_ext_ppi;
%ppi = asus_monitor_21in5_ppi;

col_width = 3.5; % inches
col_gap = 0.16; % inches

width = cols*col_width+(cols-1)*col_gap; % inches
height = hw_ratio*width*rows;

hfig = figure('Renderer', 'painters', 'Units', 'pixels', ...
    'Position', ppi*[3 3 width height]);

%set(hfig,"Units","inches")
%set(hfig,'Units','inches','Position',[3 3 width hw_ratio*width])

set(hfig,'defaultLineLineWidth',1.5) 
set(hfig,'DefaultaxesLineWidth', 1.5) 
set(hfig,'DefaultaxesFontSize', fsize) 
set(hfig,'DefaultaxesFontWeight', 'normal') 
set(hfig,'DefaultTextFontSize', fsize) 
set(hfig,'DefaultaxesFontName', 'Times new Roman') 
set(hfig,'DefaultlegendFontName', 'Times new Roman')
set(hfig,'defaultAxesXGrid','on') 
set(hfig,'defaultAxesYGrid','on') 

set(findall(hfig,'-property','Box'),'Box','off') % optional
set(findall(hfig,'-property','Interpreter'),'Interpreter','latex')
set(findall(hfig,'-property','TickLabelInterpreter'),'TickLabelInterpreter','latex')

set(hfig,'PaperPositionMode','Auto','PaperUnits','inches','PaperSize',[width,height])

%set(findall(hfig,'-property','FontSize'),'FontSize',fontsize);
set(hfig,'DefaultLineMarkerSize',3); %// The default is usually 6
fontsize(hfig,fsize,'points');

end
```

Then to save @fig:mlsave

```{.matlab #fig:mlsave caption="Save matlab figure"}
print(hfig,fullfile(fdir,fname),'-dpng','-vector')
```

## Equations ##

  * https://web.cs.ucdavis.edu/~amenta/w10/writingman.pdf

WHAT'S WRONG WITH THESE EQUATIONS? @mermin1989s is an unofficial guide
to how to include equations in prose. It is summerised as:
  
  1. Number every equation because you or someone may want to refer to
     it later.
  2. Refer to equations with a descriptive label and the number. If
     this can not easily be done, consider whether you need that
     equation or crossreference at all.
  3. Use punctuation to include equations as part of prose.

## Numbers and Units ##

I try to avoid putting hard numbers into the text. When generating
plots that require numbers in the captions, I try to generate the
caption within the same program. I also try to generate tables using
code. The goal is to avoid updating the code or figures without
updating numbers in the text. If I have to put numbers in the text I
avoid repitition.

When necessary to include numbers in tex use proper units through the
siunitx package @Lst:test.

```{#lst:test .latex caption="Examples of units in latex"}
\si{kg.s^{-1}}
\si{\kilogram\meter\per\second\squared}
\si[per-mode=symbol]{\kilogram\per\second}
```

## Presentation ##

  * https://www.youtube.com/watch?v=B2t2a7IzJMU
  * https://www.youtube.com/watch?v=PgOD1j2DhNg

  * https://www.youtube.com/watch?v=4xuiDevjT9g
  * Slide Design (MOVIE)
      * Message
          * place main message in title
      * Organize
          * pyramid main message -> supporting details
          * if long list supporting details, group into subtitles
      * Insights
		  * make your insights clear
		  * state in titles/subtitles
		  * highlight w/ bolded text, color, arrows, and lines
	  * Extras
		  * alignment and spacing
		  * units, sources, footnotes
		  
  * "If in trouble use a bubble" (text call out)

## Poster ##

  * TODO: better poster

## Other Thoughts ##

  * Published > Perfect
  * Sooner > Better
  * Try to split work into the smallest publishable units
  * Do not use linear story telling
	* Reader should not have to turn to page 2 to figure out what the
      point of your paper is or if they want to read it.
    * The intro should could contain a summary of problem, proposed
      solution, and success evalution.
    * The first sentence should make the paper's subject clear.
    * The first figure should be on page one and show the most
      impressive results. Preferably a photo of the system operating
      in the proposed environment.
    * Think BLUF (Bottom Line Up Front)



[^6]: Saying things in plain language helps you understand how good of
    a grasp you actually have on the subject.

[^7]: This shows your background knowledge. Need to define it all later.

[^8]: I prefer to lean on references rather than restate the work. 


