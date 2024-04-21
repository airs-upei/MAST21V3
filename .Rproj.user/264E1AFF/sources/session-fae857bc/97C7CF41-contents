

#' Run the MAST21 2024 protocol
#'
#' @param app_name
#' @param language
#' @param musicassessr_aws
#' @param data_collection_method
#' @param get_p_id
#' @param final_qualtrics_url
#' @param opening_and_final_image
#'
#' @return
#' @export
#'
#' @examples
#'
#'
deploy_MAST21V3_2024 <- function(
    app_name = paste("UPEI ", format(Sys.Date(), "%Y"), " Study"),
    language,
    musicassessr_aws = FALSE,
    absolute_url = "https://musicog.ca/",
    data_collection_method = "audio",
    get_p_id = FALSE,
    final_qualtrics_url = 'https://upeiairs.qualtrics.com/jfe/form/SV_5vDAjJhxLqZw7Km?participant=',
    opening_and_final_image = "https://img.freepik.com/free-vector/headphone-concept-illustration_114360-2132.jpg?w=826&t=st=1708543460~exp=1708544060~hmac=7a9cba8f7104f82422a55f30f5120598e4ce64dd222a1247c8da79825dddacb6"
) {



  after_tl <- after_setup(
    get_p_id = get_p_id,
    absolute_url = absolute_url,
    data_collection_method = data_collection_method,
    final_qualtrics_url = final_qualtrics_url,
    language = language
  )


  welcome_pg <- psychTestR::one_button_page(shiny::tags$div(shiny::tags$h2(paste("Welcome to the UPEI ", 	format(Sys.Date(), "%Y"), " Singing Test")),
                                                            shiny::tags$img(src = opening_and_final_image, height = 200, width = 200)))


  before_tl <- upei_intro(musicassessr_state)


  musicassessr::make_musicassessr_test(
    welcome_page = welcome_pg,
    elts = after_tl,
    # elts = aft,
    elts_before_setup_pages = before_tl,
    title = paste("UPEI ", format(Sys.Date(), "%Y"), " Singing Test"),
    admin_password = "demo",
    languages = language,
    opt = musicassessr::musicassessr_opt(app_name = app_name,
                                         get_p_id = get_p_id,
                                         midi_input = data_collection_method == "midi",
                                         record_audio = data_collection_method == "audio",
                                         musicassessr_aws = musicassessr_aws,
                                         setup_options =  musicassessr::setup_pages_options(input_type = if(data_collection_method == "midi") "midi_keyboard" else if(data_collection_method == "audio") "microphone" else "key_presses",
                                                                                           headphones = TRUE,
                                                                                           get_instrument_range = FALSE,
                                                                                           SNR_test = TRUE,
                                                                                           absolute_url = character()
                                                                                           )
    )
  )


}



#' Run the MAST21 2024 v2 protocol
#'
#' @param app_name
#' @param language
#' @param musicassessr_aws
#' @param data_collection_method
#' @param get_p_id
#' @param final_qualtrics_url
#' @param opening_and_final_image
#'
#' @return
#' @export
#'
#' @examples
#'
#'
deploy_MAST21V3_2024_v2 <- function(
    app_name = paste("UPEI ", format(Sys.Date(), "%Y"), " Study"),
    language,
    musicassessr_aws = FALSE,
    # absolute_url = "https://musicog.ca/",
    data_collection_method = "audio",
    get_p_id = FALSE,
    final_qualtrics_url = 'https://upeiairs.qualtrics.com/jfe/form/SV_5vDAjJhxLqZw7Km?participant=',
    opening_and_final_image = "https://img.freepik.com/free-vector/headphone-concept-illustration_114360-2132.jpg?w=826&t=st=1708543460~exp=1708544060~hmac=7a9cba8f7104f82422a55f30f5120598e4ce64dd222a1247c8da79825dddacb6"
) {




  after_tl <- after_setup_v2(
    get_p_id = get_p_id,
    # absolute_url = absolute_url,
    data_collection_method = data_collection_method,
    final_qualtrics_url = final_qualtrics_url,
    language = language
  )


  welcome_pg <- psychTestR::one_button_page(shiny::tags$div(shiny::tags$h2(paste("Welcome to the UPEI ", 	format(Sys.Date(), "%Y"), " Singing Test")),
                                                            shiny::tags$img(src = opening_and_final_image, height = 200, width = 200)))


  before_tl <- upei_intro(musicassessr_state)


  musicassessr::make_musicassessr_test(
    welcome_page = welcome_pg,
    elts = after_tl,
    # elts = aft,
    elts_before_setup_pages = before_tl,
    title = paste("UPEI ", format(Sys.Date(), "%Y"), " Singing Test"),
    admin_password = "demo",
    languages = language,
    opt = musicassessr::musicassessr_opt(app_name = app_name,
                                         get_p_id = get_p_id,
                                         midi_input = data_collection_method == "midi",
                                         record_audio = data_collection_method == "audio",
                                         musicassessr_aws = musicassessr_aws,
                                         setup_options = musicassessr::setup_pages_options(input_type = if(data_collection_method == "midi") "midi_keyboard" else if(data_collection_method == "audio") "microphone" else "key_presses",
                                                                                           headphones = TRUE,
                                                                                           get_instrument_range = FALSE,
                                                                                           SNR_test = TRUE,
                                                                                           absolute_url = character(),
                                                                                           concise_wording = TRUE)
    )
  )


}

