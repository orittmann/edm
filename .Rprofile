.First <- function() {
        dir.create(paste0(getwd(), "/figures"), showWarnings = F)
        dir.create(paste0(getwd(), "/processed-data"), showWarnings = F)
        dir.create(paste0(getwd(), "/raw-data"), showWarnings = F)
        dir.create(paste0(getwd(), "/scripts"), showWarnings = F)
        dir.create(paste0(getwd(), "/manuscript"), showWarnings = F)
        
        cat("\nWelcome to your R-Project:", basename(getwd()), "\n")
}

if (!("renv" %in% list.files())) {
        p_needed <- c("renv")
        packages <- rownames(utils::installed.packages())
        p_to_install <- p_needed[!(p_needed %in% packages)]
        if (length(p_to_install) > 0) {
                utils::install.packages(p_to_install)
        }
        lapply(p_needed, require, character.only = TRUE)
        renv::init()
        rm(list = ls())
        source("renv/activate.R")
} else {
        source("renv/activate.R")
}