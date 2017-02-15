Application Builder
===================

Case Study - Projector
----------------------
Projector is a code editor which is built around the idea of project folders.

 * create application
   * name: Projector
   * provide: Edit.Text.Code
   * provide: Browse.Folder
   * select: Data.KeyValue (default)
   * select: Data.Document (default)
   * select: Action.Menu (default)
   * select: Action.Bar (default)
   * select: Action.Shortcut (default)
   * select: Edit.Text.Code (default)
   * select: Browse.Folder (default)
   * create view
     * name: Projector.Editor
     * option: allow as window
       * enable action menu
       * enable action bar
       * enable action shortcut
     * layout: top-to-bottom
       * layout: right-to-left
         * document-view
         * project-browser
       * status-bar
       * status-bar below:
         * layout:
           * 
     * choose default action menu
     * choose default action bar
     * choose default action shortcut
     * choose status bar (bottom)
     * choose tab view (right)
     * choose 
     
