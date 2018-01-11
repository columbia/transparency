## Web transparency research at Columbia

Today’s Web services leverage users’ information – such as emails, search logs, or locations – and use them to target advertisements, prices, or products at users. Presently, users have little insight into how their data is used for such purposes. To enhance transparency, we are building a new set of tools system that detect what data – such as emails or searches – is used to target which ads in Gmail, which prices in Amazon, etc. The insight is to compare ads/prices witnessed by different accounts with similar, but not identical, subsets of the data.

### XRay

the first tool for revealing personal data use on the Web. It reveals which specific data inputs (such as emails) are used to target which outputs (such as ads). It is general and can track data use both within and across arbitrary Web services. The key idea behind XRay is to detect targeting through black-box input/output correlation. XRay populates a series of extra accounts with subsets of the inputs and then looks at the differences and commonalities between the outputs that they get in order to obtain correlation.

* Mathias Lecuyer, Guillaume Ducoffe, Francis Lan, Andrei Papancea,
Theofilos Petsios, Riley Spahn, Augustin Chaintreau, and Roxana Geambasu. 
"XRay: Increasing the Web's Transparency with Differential Correlation."
In Proceedings of the USENIX Security Symposium, San Diego, CA, August 2014.
<a href="{{ site.baseurl }}/public/usenix14lecuyer.pdf" target="_top">[PDF]</a>
* Extended version of the USENIX Security paper:
Mathias Lecuyer, Guillaume Ducoffe, Francis Lan, Andrei Papancea,
Theofilos Petsios, Riley Spahn, Augustin Chaintreau, and Roxana Geambasu.
"XRay: Increasing the Web's Transparency with Differential Correlation."
<a href="http://arxiv.org/abs/1407.2323" target="_top">Technical report</a>, July 2014.
* New York Times Technology Blog article: Steve Lohr, "XRay: A New Tool for Tracking the Use of Personal Data on the Web," August 2014. <a href="http://bits.blogs.nytimes.com/2014/08/18/xray-a-new-tool-for-tracking-the-use-of-personal-data-on-the-web/" target="_top">link</a>.
* The code is on <a href="https://github.com/columbia/xray" target="_top">Github</a>.

### Sunlight

Sunlight is an analysis pipeline that provides causal targeting detection with statistical confidence, and at scale. In the paper, we propose a 4 steps pipeline to form and assess targeting hypotheses. Our pipeline is build in a modular way, and allows extensive comparison of different algorithms. We highlight a fundamental scalability trade-off between the number of hypotheses we can make and the confidence we have in these hypotheses.

<ul>
  <li><a href="https://roxanageambasu.github.io/publications/ccs2015sunlight.pdf">
    The paper</a></li>
  <li><a href="https://github.com/columbia/sunlight">
    Sunlight source code</a></li>
  <li><a href="https://github.com/columbia/sunlight_plugin">Modified AdBlock plugin</a>  (for Web ads experiment)</li>
  <li>Data dumps: <a href="http://www.cs.columbia.edu/~mathias/sunlight/gmail/data.zip">[Gmail ads data]</a>, <a href="www.cs.columbia.edu/~riley/sunlight/website_dump.tar.gz">[Web ads data]</a></li>
</ul>

### The team

<p>
<a href="http://www.cs.columbia.edu/~mathias/">Mathias Lecuyer</a>,
<a href="http://www.cs.columbia.edu/~riley/">Riley Spahn</a>,
<a href="http://www.cs.columbia.edu/~yannis/">Yannis Spiliopoulos</a>,
<a href="http://www.cs.columbia.edu/~augustin/">Augustin Chaintreau</a>,
<a href="http://www.cs.columbia.edu/~roxana/">Roxana Geambasu</a>,
<a href="http://www.cs.columbia.edu/~djhsu/">Daniel Hsu</a>
</p>
