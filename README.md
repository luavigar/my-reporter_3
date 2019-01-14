<div class="Box-body p-6">
        <article class="markdown-body entry-content" itemprop="text"><h1><a id="user-content-testcafe-reporter-html-testrail" class="anchor" aria-hidden="true" href="#testcafe-reporter-html-testrail"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>testcafe-reporter-html-testrail</h1>
<p>This is the <strong>html-testrail</strong> reporter plugin for <a href="http://devexpress.github.io/testcafe" rel="nofollow">TestCafe</a>.</p>
<p align="center">
    <a target="_blank" rel="noopener noreferrer" href="https://raw.yomismo.com/yomismo/HTML-TestRail/master/media/Console_Output.jpg"><img src="https://raw.yomismo.com/yomismo/HTML-TestRail/master/media/Console_Output.jpg" alt="preview" style="max-width:100%;"></a>
</p>
<h2><a id="user-content-install" class="anchor" aria-hidden="true" href="#install"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Install</h2>
<pre><code>npm install testcafe-reporter-html-testrail
</code></pre>
<h2><a id="user-content-usage" class="anchor" aria-hidden="true" href="#usage"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Usage</h2>
<p>When you run tests from the command line, specify the reporter name by using the <code>--reporter</code> option:</p>
<pre><code>testcafe chrome 'path/to/test/file.js' --reporter html-testrail
</code></pre>
<p>When you use API, pass the reporter name to the <code>reporter()</code> method:</p>
<div class="highlight highlight-source-js"><pre>testCafe
    .<span class="pl-en">createRunner</span>()
    .<span class="pl-en">src</span>(<span class="pl-s"><span class="pl-pds">'</span>path/to/test/file.js<span class="pl-pds">'</span></span>)
    .<span class="pl-en">browsers</span>(<span class="pl-s"><span class="pl-pds">'</span>chrome<span class="pl-pds">'</span></span>)
    .<span class="pl-en">reporter</span>(<span class="pl-s"><span class="pl-pds">'</span>html-testrail<span class="pl-pds">'</span></span>) <span class="pl-c"><span class="pl-c">//</span> &lt;-</span>
    .<span class="pl-en">run</span>();</pre></div>
<h2><a id="user-content-additional-configuration" class="anchor" aria-hidden="true" href="#additional-configuration"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Additional Configuration</h2>
<h4><a id="user-content-for-html-report" class="anchor" aria-hidden="true" href="#for-html-report"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>For HTML Report</h4>
<pre><code>HTML_REPORT_PATH : set the report output folder | default: Node_modules's (in where plugin is installed) sibling folder
HTML_REPORT_Name : set the report name | default: Report_TIMESTAMP.html (e.g.: Report_16_5_2018_14_46_46.html)
</code></pre>
<h5><a id="user-content-sample-report" class="anchor" aria-hidden="true" href="#sample-report"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Sample Report</h5>
<p align="center">
    <a target="_blank" rel="noopener noreferrer" href="https://camo.githubusercontent.com/fd50a4ef18e3690e56e9807d6bfb3a3f65b21843/68747470733a2f2f7261772e6769746875622e636f6d2f6d6974657368736176616e692f48544d4c2d546573745261696c2f6d61737465722f6d656469612f48544d4c5f4f75747075742e6a7067"><img src="https://camo.githubusercontent.com/fd50a4ef18e3690e56e9807d6bfb3a3f65b21843/68747470733a2f2f7261772e6769746875622e636f6d2f6d6974657368736176616e692f48544d4c2d546573745261696c2f6d61737465722f6d656469612f48544d4c5f4f75747075742e6a7067" alt="preview" data-canonical-src="https://raw.github.com/miteshsavani/HTML-TestRail/master/media/HTML_Output.jpg" style="max-width:100%;"></a>
</p>
<h4><a id="user-content-for-testrail-publish" class="anchor" aria-hidden="true" href="#for-testrail-publish"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>For Testrail publish</h4>
<p>Before using Testrail publisher, You need to set test description in <code>specific format</code> as per bleow.</p>
<h5><a id="user-content-format" class="anchor" aria-hidden="true" href="#format"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Format:</h5>
<pre><code>test('&lt;&lt; Group Name&gt;&gt; | &lt;&lt; Test Name &gt;&gt; | &lt;&lt; Testrail Case_ID &gt;&gt; ', async t =&gt; { .... });

&lt;&lt; Group Name &gt;&gt; - It can be any like Smoke, sanity, functional.
&lt;&lt; Test Name &gt;&gt;  - Test name of that test cases
&lt;&lt; Testrail Case_ID &gt;&gt;  - case ID of testrail's test case (The testcase should be present in the given PROJECT_NAME)

Example:

test('Smoke | Verify the Login Page | C875986 ', async t=&gt; { ... });
</code></pre>
<p><code>Assumption</code>: Testrail should contains Project which you will set as PROJECT_NAME and All the Automation test cases should present in the Testrail(that Case_ID will you set in the test description)</p>
<h5><a id="user-content-environment-variables" class="anchor" aria-hidden="true" href="#environment-variables"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Environment Variables</h5>
<pre><code>TESTRAIL_ENABLE : set true to enable Testrail api | default: false
TESTRAIL_HOST : https://mitesh.testrail.com/ 
TESTRAIL_USER : username
TESTRAIL_PASS : password or api key
PROJECT_NAME : project name
PLAN_NAME : plan name | default: TestAutomation_1
</code></pre>
<p><code>Note:</code> If you do not specify the <code>PLAN_NANE</code> then plugin will create <code>TestAutomation_1</code> plan name (if not exist) in the given Project</p>
<h2><a id="user-content-author" class="anchor" aria-hidden="true" href="#author"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Author</h2>
<p>Mitesh Savani (<a href="https://github.com/miteshsavani">https://github.com/miteshsavani</a>)</p>
</article>
      </div>
