<div class="span12">			

<div class="tl-unit-content ">
	<div style="display: none;" id="last-unit-progress"></div>
	<div style="display: none;" id="assignment-reply-type"></div>
	<div class="hide" id="assignment-modify-answer-time"></div>
	<div class="tl-unit-content ">
		<center><div class="readability"><h1 id="exercise-classes">Exercise: Classes</h1>
<div class="wincpy">
<p><code class="interpreted-text" role="command">wincpy start 04da020dedb24d42adf41382a231b1ed</code></p>
</div>
<p>In this exercise you will make use of Object Oriented Programming. Books have been written about this subject, and some of them may even be worth reading. For now it suffices
to say that you are going to declare and use a number of classes that are going to interact with each other. It's a difficult one, so take your time!</p>
<h2 id="part-1-players">Part 1: Players</h2>
<ol type="1">
<li>
<p>In <code>main.py</code>, write a class <code>Player</code> that is going to represent a soccer player.</p>
</li>
<li>
<p>Define the <code>Player</code> class' initialization method (<code>__init__</code>) such that it can receive these arguments, in this order:</p>
<ul>
<li>name (<code>str</code>)</li>
<li>speed (<code>float</code> between 0 and 1)</li>
<li>endurance (<code>float</code> between 0 and 1)</li>
<li>accuracy (<code>float</code> between 0 and 1)</li>
</ul>
<p>If speed, endurance or accuracy is not between 0 and 1 (inclusive), a <code>ValueError</code> must be raised.</p>
<p>Save the given arguments as instance attributes under the names <code>name</code>, <code>speed</code>, <code>endurance</code> and <code>accuracy</code>.</p>
</li>
<li>
<p>Define an <code class="interpreted-text" role="term">instance method</code> <code>introduce</code> that takes no arguments (except <code>self</code>!) and returns a string like
the following, where <code>'Bob'</code> is replaced by the player's actual name:</p>
<p><code>'Hello everyone, my name is Bob.'</code></p>
</li>
<li>
<p>Define an instance method <code>strength</code> that takes no arguments and returns a tuple like the following, where the string <code>speed</code> is replaced by the player's
actual highest attribute and the value corresponds to that attribute:</p>
<p><code>('speed', 0.8)</code></p>
<p>If multiple attributes share the same value, prioritize as follows:</p>
<p><code>speed &gt; endurance &gt; accuracy</code></p>
</li>
</ol>
<h2 id="part-2-commentators">Part 2: Commentators</h2>
<ol type="1">
<li>
<p>In <code>main.py</code>, create a new class <code>Commentator</code>.</p>
</li>
<li>
<p>Implement it in such a way that we can do this:</p>
<div class="sourceCode" id="cb1">
<pre class="sourceCode python"><code class="sourceCode python"><span id="cb1-1"><a href="#cb1-1" aria-hidden="true"></a>ray <span class="op">=</span> Commentator(<span class="st">'Ray Hudson'</span>)</span>
<span id="cb1-2"><a href="#cb1-2" aria-hidden="true"></a><span class="bu">print</span>(ray.name)</span>
<span id="cb1-3"><a href="#cb1-3" aria-hidden="true"></a><span class="co"># 'Ray Hudson'</span></span></code></pre></div>
</li>
<li>
<p>Write an instance method <code>sum_player</code> that takes an instance of a player and returns the sum of their <code>speed</code>, <code>endurance</code> and
<code>accuracy</code> attributes.</p>
<p>To do this you may need the function <code>getattr</code>: <a href="https://stackoverflow.com/a/55609455/7613292">The Python getattr Function</a>.</p>
</li>
<li>
<p>Write an instance method <code>compare_players</code> that takes two instances of <code>Player</code> (in no particular order) and one of <code>'speed'</code>,
<code>'endurance'</code> and <code>'accuracy'</code> as its arguments and returns the name of the player that scores the highest on this attribute. For example:</p>
<div class="sourceCode" id="cb2">
<pre class="sourceCode python"><code class="sourceCode python"><span id="cb2-1"><a href="#cb2-1" aria-hidden="true"></a>alice <span class="op">=</span> Player(<span class="st">'Alice'</span>, <span class="fl">0.8</span>, <span class="fl">0.2</span>, <span class="fl">0.6</span>)</span>
<span id="cb2-2"><a href="#cb2-2" aria-hidden="true"></a>bob <span class="op">=</span> Player(<span class="st">'Bob'</span>, <span class="fl">0.9</span>, <span class="fl">0.2</span>, <span class="fl">0.6</span>)</span>
<span id="cb2-3"><a href="#cb2-3" aria-hidden="true"></a><span class="bu">print</span>(ray.compare_players(alice, bob, <span class="st">'speed'</span>))</span>
<span id="cb2-4"><a href="#cb2-4" aria-hidden="true"></a><span class="co"># 'Bob'</span></span></code></pre></div>
<p>If the players score equally on this attribute, return the name of the player that has the highest strength according to the <code>strength</code> function you just
implemented.</p>
<p>If these are <em>also</em> equal, report the name of the player that has the highest total score according to the <code>sum_player</code> function you just implemented.</p>
<p>If these are <em>also</em> equal, return the string:</p>
<p><code>'These two players might as well be twins!'</code></p>
</li>
</ol>
<h2 id="wincpy-check">Wincpy Check</h2>
<p>Use <code>wincpy check classes</code> to see if you met all of the requirements for this exercise. Did you pass the test?</p></div></center>			</div>
	
