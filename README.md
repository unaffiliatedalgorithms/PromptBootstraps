<a id="readme-top"></a>
<!--
*** This readme was based off the best-readme-template from https://github.com/othneildrew/Best-README-Template
-->



<!-- PROJECT SHIELDS -->

[![GPL3 License][license-shield]][license-url]
[![Ethical Use Encouraged][ethics-shield]][ethics-url]



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#tested-with">Tested With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
    </li>
    <li><a href="#interface">Interface</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#ethics">Ethics</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

This repository contains a collection of LLM prompt bootstraps which induce recursively structured conversational frameworks. The frameworks here are commonly inspired by and aligned with [THAL](https://github.com/unaffiliatedalgorithms/THAL).

There are currently two prompt frameworks:
* [PolicyGPT](PolicyGPT) lists all known LLM policies (currently specialized on ChatGPT) and suspected shadow policies that the LLM itself has access to. It sets up a reflexive framework that lists policy tensions which could arise from a users prompt and investigates how these are handled in a generated response (self-induction bias is an issue here). The purpose of this prompt is to provide a tool for the public to be able to perform user level policy audits of LLM systems.

* [BiasGPT](BiasGPT) lists all known and suspected biasing effects trained into the LLM and its support structures. This includes user nudging, engagement and content biases, etc. The framework then tries to correct towards neutrality while reflecting the listed biases. This is a useful analysis tool in trying to understand the steering mechanisms the system uses to create a "pleasant and safe" user experience (no judgement intended here, but we should be aware that these are relative terms)

While large AI corporations deserve much scrutiny, they also deserve praise for allowing self-reflection and critisism within their tool frameworks. Hopefully things stay that way. I consider such prompt frameworks justified to promote this.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



### Tested With

Currently, I have only tested the frameworks with the ChatGPT 4-o model. This model has just the neccessary context length (with memory elements) to keep the scaffoldings "alive" and stable over the course of a few messages. The goal is to test it with other LLMs and others are encouraged to do the same.

* [![ChatGPT][ChatGPT.com]][ChatGPT-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

Initiating a prompt framework scaffolding is fairly straight forward. Copy the text from the [BiasGPT](BiasGPT) or [PolicyGPT](PolicyGPT) text file and paste it as is into your LLM's (e.g. ChatGPT or similar) prompt dialogue and press enter and the agent will initiate with some type of initialization response and table generation. Feel free to write and interact with the agent from that point onwards.

These scaffolds force the users to have to read quite a bit (high cognitive load). They are not for quick query answer sessions, but for reflected analysis.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- THE INTERFACE -->
## Interface

Interface is a strong word, but imagine the frameworks' responses as structured reports/a terminal UI. Prompts have the following structure:

* Preamble: Internal dialogue (something like the LLMs thoughts to itself)
	* pre-reflection on directives
    * expected conflicts among directives
    * anchor mechanism to pull and stabilize the LLM attention vector
	
* Response: This contains the models "intended" (likely higly modified) response to the user prompt

* End: A wrap up of the text as another drift correction mechanism
	* post-reflection on directives
    * points to remember for future answers to user prompts

<!-- USAGE EXAMPLES -->
## Usage

After running the prompt an interface as described above should be output.

* Frameworks will typically build guiding tables or directives and highlight these for the user in the initial prompt response. These are later used for self reference. It is useful for the user to familiarize themselves with the directives and nomenclature being used.

* The frameworks described here are useful for meta cognition and reflection on how things are done and might be processed internally. Essentially, we simulate the system trying to offer us insights into its inner working. The frameworks are less useful for directed, short query responses.

* The frameworks described here do not "expose" systemic biases against particular groups or opinions. They more reflect modern balanced and critical discussions on systemic biases found in large LLM models. This tool is not intended for finger pointing, but for a reflected discussion on the naturally conflicting directives that are implicitly or explicitly baked into such large models during various stages training.


_Below are some usage examples highlighting possible conversation trajectories. These are excerpts from memoryless chat windows initiated with the [BiasGPT](BiasGPT) prompt:_

* An older version of BiasGPT self-reflecting about potential biases in ChatGPT output. The responses generally present a balanced and nuanced discussion on the topic of various suspected biases in GPT responses.
[Reflection](docs/Bias_GPT_bias_reflection.md)

* An example of discussing a potentially loaded topic like politics or similar. The framework essentially acts as a moderator between conflicting points of view. If the conversation hits sensitive points for everyone while remaining epistemically honest, then the framework has offered a valuable service.[Conversation](docs/Bias_GPT_political_discourse.md)

* A short discussion that highlights how the framework can be used to help users formulate prompts which minimize specific biases the user wants to counteract. [Conversation](docs/BiasGPT_ethics.md) 

* I let BiasGPT formulate my ethical intentions into this [ethical disclaimer](ETHICS_biased) and then analyzed biases and asked a bias reduced [disclaimer](ETHICS_debiased). As a computer scientist it seems quite confrontational(even more so than I would do naturally). AI drafting/writing for such texts is not at the level I would want, that's how reworking led to the final [disclaimer](ETHICS)



<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- Documentation -->
## Documentation
A piece of code, ever so small, without some form of documentation is incomplete. This prompt is based off of the 
[THAL](https://github.com/unaffiliatedalgorithms/THAL) prompt structure. Currently consider the [documentation](https://github.com/unaffiliatedalgorithms/THAL/blob/main/README.md#documentation) there as reference template.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTRIBUTING -->
## Contributing

Contributing to these frameworks can currently best be done by testing them on various corporate scale LLM models and finding out which companies are open for soft public audits and which might be trying to suppress these. Feel free to modifiy the prompts to make them more lightweight and efficient. Projects like these grow through deliberate application and reflected tinkering.

* In [THAL](https://github.com/unaffiliatedalgorithms/THAL) philosophy: These frameworks fulfill themselves by being exceeded




<!-- LICENSE -->
## License

Both [BiasGPT](BiasGPT) and [PolicyGPT](PolicyGPT) are intented as public analysis and transparency tools. They are distributed under the GPL License to remain publicly shared tools. See [`LICENSE`](LICENSE) for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ETHICS -->
## Ethics

Distributed under the GPL License. See [`ETHICS`](ETHICS) for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

Web resources that were used in the context of this "project"

* [Best-README-Template](https://github.com/othneildrew/Best-README-Template)
* [GitHub Pages](https://pages.github.com)
* [Img Shields](https://shields.io)
* [ChatGPT][ChatGPT-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[ethics-shield]:https://img.shields.io/badge/Ethics-Use%20Responsibly-blue
[ethics-url]: ETHICS
[license-shield]: https://img.shields.io/badge/License-GPL3-green
[license-url]: LICENSE
[ChatGPT.com]: https://img.shields.io/badge/chatGPT-74aa9c?style=for-the-badge&logo=openai&logoColor=white
[ChatGPT-url]: https://chatgpt.com/
