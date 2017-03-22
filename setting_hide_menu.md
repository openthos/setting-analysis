
# 如何在settings中隐藏已经存在的某些项目

settings所有项目的布局加载文件为xml/dash_category.xml，如果想要隐藏某些模块不是简单的在xml/dash_category.xml里删掉或注释掉就可以了，因为在某些情况下，万一这个模块，在其他代码中使用了其中的id,当注释或删除此块代码，牵一发而动全身，所以要从整个模块加载流程入手：

 - 首先通过一个方法加载并部署该dashboradcagegory
    
    SettingsActivity.java
    
        categories.clear();
        loadCategoriesFromResource(R.xml.dashboard_categories, categories);
        updateTilesList(categories);
    }
    
  - 
