# classes

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
	<div class="clear"></div>
		<div id="tl-complete-unit-handles-area" class="text-center  ">
		<hr class="tl-hr-content">
				<div class="tl-completed-unit-handles" style="">
			<div class="btn-group dropup" style="display: inline-block;">
							<a href="javascript:void(0)" class="btn btn-large tl-passed-continue-unit-button" onclick="location='https://board.wincacademy.nl/unit/view/id:5202'">Completed. Let's continue.</a>
			
						</div>
								</div>
		
				<div class="tl-pending-unit-handles" style="display:none">
			<a href="javascript:void(0)" class="btn btn-large tl-pending-button-assignment disabled">Pending reply from Instructor</a>
			<div class="help-inline tl-assignment-more-options-pending">
				<div class="tl-assignment-handles-inner">
					<div class="tl-assignment-icon tl-assignment-check-answer">
						<div class="tl-icon-stack">
							<i class="icon-circle tl-icon-stack-background"></i>
							<i class="icon-comment tl-icon-stack-content"></i>
						</div>
						<br class="clear">
						<div class="tl-icon-label">Your answer</div>
					</div>
					<div class="tl-assignment-icon tl-assignment-modify-answer">
						<div class="tl-icon-stack">
							<i class="icon-circle tl-icon-stack-background"></i>
							<i class="icon-edit tl-icon-stack-content"></i>
						</div>
						<br class="clear">
						<div class="tl-icon-label">Modify your answer</div>
					</div>
				</div>
			</div>
		</div>
				
				
				
		<div class="tl-incomplete-unit-handles" style="display:none">
											<a href="javascript:void(0)" class="btn btn-large tl-complete-button tl-completed-continue-button" data-toggle="https://board.wincacademy.nl/unit/complete/id:5194">Complete and continue</a>
									
		</div>
	</div>
		
	</div>

<div class="modal fade" id="tl-course-completed-modal" style="display: none; outline: none;" tabindex="-1">
    <div class="modal-body text-center">
     	<a href="javascript:void(0)" class="close pull-right" data-dismiss="modal">×</a>
		<h1>Congratulations!</h1>
		<img alt="Course completed!" src="https://d3j0t7vrtr92dk.cloudfront.net/images/course_completed.jpg">
		<h2>Course completed!</h2>
    	<h3><span title="Back-end Development" class="tl-formatted-course-name">Back-end Development</span></h3>
           		<div id="tl-course-completed-modal-options" class="text-center">
        	        	<p><a class="btn btn-primary tl-download-certificate" href="https://board.wincacademy.nl/user/downloadcertification/id:###id###" style="display: none;">Download certificate</a></p>
        	        							<p><a class="tl-courses-list" href="https://board.wincacademy.nl/dashboard/index">Go to course list</a></p>
			        	        	<p><a class="tl-next-course" href="https://board.wincacademy.nl/learner/courseinfo/id:###id###" style="display:none">Go to next course</a></p>
        	        	</div>
        </div>
</div>

<div class="modal fade hide" id="tl-course-failed-modal" style="outline: none;" tabindex="-1">
    <div class="modal-body text-center">
        <a href="javascript:void(0)" class="close pull-right" data-dismiss="modal">×</a>
		<h1>You didn't quite make it</h1>
		<img alt="You didn't quite make it" src="https://d3j0t7vrtr92dk.cloudfront.net/images/course_failed.png">
		<h2>Unfortunately, you didn't reach a passing score for this course</h2>
	       <div id="tl-course-failed-modal-options" class="text-center">
								<p><a class="tl-courses-list" href="https://board.wincacademy.nl/dashboard/index">Go to course list</a></p>
			        </div>
	    </div>
</div>



<script>
	var tl_timer_id = false;
	var isCompleted = false;
	var unitEndDate;


$(document).ready(function(){
	
	if($('#tl-gamification-points-message').length){
		$('#tl-gamification-points-message').css('z-index','10000');
	}

	if($('#tl-gamification-badges-message').length){
		$('#tl-gamification-badges-message').css('z-index','10000');
	}
	
	if ($('#documents-images-zip_namespace').length) {
		$('#documents-images-zip_namespace').fileupload({
			autoUpload: true,
			disableInputButton: false,
			replaceFileInput: true,
			acceptFileTypes: /(\.|\/)(gif|jpg|jpeg|png|ppt|pptx|doc|docx|xls|xlsx|pdf|zip|mp4|webm|ogg|ogv|avi|mpeg|mpg|mov|wmv|3gp|flv|mp3|aac|ogg|oga|wav|mpeg|webm|wma|aif|aiff)$/i,
			maxFileSize: 209715200,
			maxFileSizeArray: uploader_limits,
			add: function(e, data){
					$('.tl-assignment-showuploader').click(); // Show file form.
					var that = this;
					var $this = $(this);
					var validation = data.process(function () {
						return $this.fileupload('process', data);
					});
					validation.done(function() {
						$.blueimp.fileupload.prototype.options.add.call(that, e, data);
					});
					validation.fail(function(data) {
						$('#documents-images-zip_namespace .note.error').html("<i class='icon-attention-circled tl-cursor-default'></i> "+data.files[data.index].error);
					});
				},
			done: function(e, data){
				resp = $.parseJSON(data.jqXHR.responseText);
				setTimeout(function(){data.context.remove()}, 200); // remove completed file's table row
				
				if (resp.success) {
					 if(resp.data.assignmentReplyFile !== undefined){
						 completeAssignmentUnit(null, resp.data.assignmentReplyFile);
					 }
					 else {
						 $('#documents-images-zip_namespace .note.error').html("<i class='icon-attention-circled tl-cursor-default'></i> "+resp.data.error);
					 }
				}
				else {
					 $('#documents-images-zip_namespace .note.error').html("<i class='icon-attention-circled tl-cursor-default'></i> "+resp.data.error);
				 }
			}
		});
		$('#documents-images-zip_namespace').bind('fileuploadadd', function (e) {$('#documents-images-zip_namespace tr.template-upload, #documents-images-zip_namespace tr.template-download').remove();});
		$('#documents-images-zip_namespace').bind('fileuploadstart', function(e){ myportal.app.isUploading = true; });
		$('#documents-images-zip_namespace').bind('fileuploadstop', function(e){ myportal.app.isUploading = false; });
	}
	
	
	$('#send-message-instructor-failing').on('click', function(){
		$('#tl-course-failed-modal').modal('hide');
		$('#tl-send-message-modal').modal();
	});

	if ($('.tl-assignment-reply-editor').length) {
		$('.tl-assignment-reply-editor').summernote({
			airMode: true,
			airPopover: [
				['text', ['bold', 'italic', 'underline']],
				['insert', ['link', 'picture']]
			],
			disableDragAndDrop: true,
			onImageUpload: function(files) {
				return false;
			}
		});
	}

    $(document).on('blur', '.note-editable', function(){
		$('.note-air-popover').hide();
	});

	var gamificationPointsForUnitCompletion = $.cookie("gamification_points_for_unit_completion");
	var gamificationPointsForCourseCompletion = $.cookie("gamification_points_for_course_completion");
	var gamificationPointsForCertification = $.cookie("gamification_points_for_certification");
	var gamificationPointsNotification = '';
	var gamificationAddedPoints = 0;

	if(gamificationPointsForUnitCompletion){
		var parts = gamificationPointsForUnitCompletion.split('###');
		gamificationPointsNotification = parts[0];
		gamificationAddedPoints = parseInt(parts[1]);
		setTlmsCookie("gamification_points_for_unit_completion", null, {expires: -1, path: '/', domain: myEffectiveDomain, secure: false});
	}

	if(gamificationPointsForCourseCompletion){
		var parts = gamificationPointsForCourseCompletion.split('###');
		gamificationPointsNotification = (gamificationPointsNotification) ? gamificationPointsNotification + '<br/>' + parts[0] : parts[0];
		gamificationAddedPoints = gamificationAddedPoints + parseInt(parts[1]);
		setTlmsCookie("gamification_points_for_course_completion", null, {expires: -1, path: '/', domain: myEffectiveDomain, secure: false});
	}

	if(gamificationPointsForCertification){
		var parts = gamificationPointsForCertification.split('###');
		gamificationPointsNotification = (gamificationPointsNotification) ? gamificationPointsNotification + '<br/>' + parts[0] : parts[0];
		gamificationAddedPoints = gamificationAddedPoints + parseInt(parts[1]);
		setTlmsCookie("gamification_points_for_certification", null, {expires: -1, path: '/', domain: myEffectiveDomain, secure: false});
	}

	if(gamificationPointsNotification){
		if($("#tl-header-gamification-entrance").data('entrancemode') == 'points'){
			$("#tl-header-gamification-entrance").empty();
			var pointsCountUp = new countUp("tl-header-gamification-entrance", parseInt($("#tl-header-gamification-entrance").data('entrancevalue')) - parseInt(gamificationAddedPoints), parseInt($("#tl-header-gamification-entrance").data('entrancevalue')), 0, 1.5, {useEasing: true, useGrouping: true, separator: '', suffix: ' ' + "points"});
			pointsCountUp.start();
		}
		
		$("#tl-gamification-points-message").html(decodeURIComponent(gamificationPointsNotification)).fadeIn(1000);
		setTimeout(function(){$("#tl-gamification-points-message").fadeOut('slow');}, 3000);
	}

	var gamificationAssignmentBadge = $.cookie("gamification_assignment_badge");
	var gamificationLearningBadge = $.cookie("gamification_learning_badge");
	var gamificationCertificationBadge = $.cookie("gamification_certification_badge");

	if(gamificationAssignmentBadge){
		var parts = gamificationAssignmentBadge.split('###');
		$(".tl-badge-image").attr('src', parts[1]);
		$(".tl-badge-message").html(decodeURIComponent(parts[0]));
		setTlmsCookie("gamification_assignment_badge", null, {expires: -1, path: '/', domain: myEffectiveDomain, secure: false});
	}

	if(gamificationLearningBadge){
		var parts = gamificationLearningBadge.split('###');
		setTlmsCookie("gamification_learning_badge", null, {expires: -1, path: '/', domain: myEffectiveDomain, secure: false});

		if($(".tl-badge-image").attr('src') != '' && $(".tl-badge-message").html() != ''){
			$("#tl-gamification-badges-message").append('<hr/><div id="learning-badge-message" class="tl-badge-image-message-wrapper"></div>');
			$("#learning-badge-message").append('<img class="tl-badge-image pull-left image60x60" src="' + parts[1] + '"/>').append('<div class="tl-badge-message text-center tl-bold-item">' + decodeURIComponent(parts[0]) + '</div>');
		}
		else{
			$(".tl-badge-image").attr('src', parts[1]);
			$(".tl-badge-message").html(decodeURIComponent(parts[0]));
		}
	}

	if(gamificationCertificationBadge){
		var parts = gamificationCertificationBadge.split('###');
		setTlmsCookie("gamification_certification_badge", null, {expires: -1, path: '/', domain: myEffectiveDomain, secure: false});

		if($(".tl-badge-image").attr('src') != '' && $(".tl-badge-message").html() != ''){
			$("#tl-gamification-badges-message").append('<hr/><div id="certification-badge-message" class="tl-badge-image-message-wrapper"></div>');
			$("#certification-badge-message").append('<img class="tl-badge-image pull-left image60x60" src="' + parts[1] + '"/>').append('<div class="tl-badge-message text-center tl-bold-item">' + decodeURIComponent(parts[0]) + '</div>');
		}
		else{
			$(".tl-badge-image").attr('src', parts[1]);
			$(".tl-badge-message").html(decodeURIComponent(parts[0]));
		}
	}

	if(gamificationAssignmentBadge || gamificationLearningBadge || gamificationCertificationBadge){
		if(gamificationPointsNotification){
			$("#tl-gamification-badges-message").css('bottom', $("#tl-gamification-points-message").height() + 20 + 16 + 5);
		}

		if($("#tl-header-gamification-entrance").data('entrancemode') == 'badges'){
			$("#tl-header-gamification-entrance").empty();
			var badgesCountUp = new countUp("tl-header-gamification-entrance", 0, parseInt($("#tl-header-gamification-entrance").data('entrancevalue')), 0, 1.5, {useEasing: true, useGrouping: true, separator: '', suffix: ' ' + "badges"});
			badgesCountUp.start();
		}

		$("#tl-gamification-badges-message").fadeIn(1000).css('display', 'table');
		setTimeout(function(){$("#tl-gamification-badges-message").fadeOut('slow');}, 5000);
	}

	var gamificationCompletedCourses = $.cookie("gamification_completed_courses");

	if(gamificationCompletedCourses && $("#tl-header-gamification-entrance").data('entrancemode') == 'courses'){
		$("#tl-header-gamification-entrance").empty();
		var completedCoursesCountUp = new countUp("tl-header-gamification-entrance", 0, parseInt($("#tl-header-gamification-entrance").data('entrancevalue')), 0, 1.5, {useEasing: true, useGrouping: true, separator: '', suffix: ' ' + "completed courses"});
		completedCoursesCountUp.start();
		setTlmsCookie("gamification_completed_courses", null, {expires: -1, path: '/', domain: myEffectiveDomain, secure: false});
	}

	var gamificationUserLevel = $.cookie("gamification_user_level");

	if(gamificationUserLevel && $("#tl-header-gamification-entrance").data('entrancemode') == 'levels'){
		var gamificationUserLevelParts = gamificationUserLevel.split('###');
		$("#tl-header-gamification-entrance").empty();
		var userLevelCountUp = new countUp("tl-header-gamification-entrance", 0, parseInt(gamificationUserLevelParts[0]), 0, 1.5, {useEasing: true, useGrouping: true, separator: ''});
		userLevelCountUp.start(function(){$('#tl-header-gamification-entrance').html(decodeURIComponent(gamificationUserLevelParts[1]));});
		setTlmsCookie("gamification_user_level", null, {expires: -1, path: '/', domain: myEffectiveDomain, secure: false});
	}

		
	$('#documents-images-zip_namespace .inputbtn').addClass('btn btn-large').data('placement', 'right');
	
	$("a[rel=popover]").popover({placement: 'bottom'}).click(function(e){
		if($(this).hasClass('tl-content-show-popover')){
			e.preventDefault();
		}
	});

	$(document).on('click', '.tl-assignment-select-method', function(){
		$("#tl-recording-area").hide();
		if(videoRecordingPlayer){
			videoRecordingPlayer.record().reset();
		}
		$("#tl-recording-audio-area").hide();
		if(audioRecordingPlayer){
			audioRecordingPlayer.record().reset();
		}
		$("#tl-recording-screen-area").hide();
		if(screenRecordingPlayer){
			screenRecordingPlayer.record().reset();
		}
		$('#documents-images-zip_namespace').hide();
		$('#assignment-reply-textbox-group').hide();
		$('.tl-assignment-handles').hide();
		$('.tl-complete-button-assignment').hide();
		$('.tl-send-assignment-recording').addClass('disabled').hide();
		$('.tl-send-assignment-recording-audio').addClass('disabled').hide();
		$('.tl-send-assignment-recording-screen').addClass('disabled').hide();
		$('.tl-assignment-handles').show();
		$(this).parent().hide();
	});

    $(document).on('click', '.tl-assignment-usetextbox', function(){
		$("#tl-recording-area").hide();
		if(videoRecordingPlayer){
			videoRecordingPlayer.record().reset();
		}
		$("#tl-recording-audio-area").hide();
		if(audioRecordingPlayer){
			audioRecordingPlayer.record().reset();
		}
		$("#tl-recording-screen-area").hide();
		if(screenRecordingPlayer){
			screenRecordingPlayer.record().reset();
		}
		$('#documents-images-zip_namespace').hide();
		$('#assignment-reply-textbox-group').show();
		$('#assignment-reply-textbox-group').removeClass('hidden-textbox').addClass('visible-textbox');
		$('.tl-complete-button-assignment').show();
		$('.tl-send-assignment-recording').addClass('disabled').hide();
		$('.tl-send-assignment-recording-audio').addClass('disabled').hide();
		$('.tl-send-assignment-recording-screen').addClass('disabled').hide();
		$('.tl-assignment-select-method').parent().show();
		$('.tl-assignment-handles').hide();
		setTimeout(function(){ $("#assignment-reply-textbox").focus(); }, 100);
	});

    $(document).on('click', '.tl-assignment-showuploader', function(){
		$("#tl-recording-area").hide();
		if(videoRecordingPlayer){
			videoRecordingPlayer.record().reset();
		}
		$("#tl-recording-audio-area").hide();
		if(audioRecordingPlayer){
			audioRecordingPlayer.record().reset();
		}
		$("#tl-recording-screen-area").hide();
		if(screenRecordingPlayer){
			screenRecordingPlayer.record().reset();
		}
		$('#documents-images-zip_namespace').show();
		$('#assignment-reply-textbox-group').hide();
		$('#assignment-reply-textbox-group').removeClass('visible-textbox').addClass('hidden-textbox');
		$('#documents-images-zip_namespace').show();
		$('.tl-complete-button-assignment').hide();
		$('.tl-send-assignment-recording').addClass('disabled').hide();
		$('.tl-send-assignment-recording-audio').addClass('disabled').hide();
		$('.tl-send-assignment-recording-screen').addClass('disabled').hide();
		$('.tl-assignment-select-method').parent().show();
		$('.tl-assignment-handles').hide();
	});

	$(document).on('click', '.tl-assignment-showrecorder', function(){
		$("#tl-recording-audio-area").hide();
		if(audioRecordingPlayer){
			audioRecordingPlayer.record().reset();
		}
		$("#tl-recording-screen-area").hide();
		if(screenRecordingPlayer){
			screenRecordingPlayer.record().reset();
		}
		$('#assignment-reply-textbox-group').removeClass('visible-textbox').addClass('hidden-textbox');
		$('#documents-images-zip_namespace').hide();
		$('.tl-complete-button-assignment').hide();
		$('.tl-send-assignment-recording').addClass('disabled').show();
		$('.tl-send-assignment-recording-audio').addClass('disabled').hide();
		$('.tl-send-assignment-recording-screen').addClass('disabled').hide();
		$('.tl-assignment-select-method').parent().show();
		$('.tl-assignment-handles').hide();
		$("#tl-recording-area").show();
		if(videoRecordingPlayer){
			videoRecordingPlayer.record().getDevice();
		}
	});

	$(document).on('click', '.tl-assignment-showrecorder-audio', function(){
		$("#tl-recording-area").hide();
		if(videoRecordingPlayer){
			videoRecordingPlayer.record().reset();
		}
		$("#tl-recording-screen-area").hide();
		if(screenRecordingPlayer){
			screenRecordingPlayer.record().reset();
		}

		setTimeout(function(){
			// unlike the video recorder, we initialize the audio recorder after it is visible to the user, otherwise the sound waves do not show up
			initAudioRecordingPlayer();
		}, 100);
		$('#assignment-reply-textbox-group').removeClass('visible-textbox').addClass('hidden-textbox');
		$('#documents-images-zip_namespace').hide();
		$('.tl-complete-button-assignment').hide();
		$('.tl-send-assignment-recording').addClass('disabled').hide();
		$('.tl-send-assignment-recording-screen').addClass('disabled').hide();
		$('.tl-send-assignment-recording-audio').addClass('disabled').show();
		$('.tl-assignment-select-method').parent().show();
		$('.tl-assignment-handles').hide();
		$("#tl-recording-audio-area").show();
		if(audioRecordingPlayer){
			audioRecordingPlayer.record().getDevice();
		}
	});

	$(document).on('click', '.tl-assignment-showrecorder-screen', function() {
		$("#tl-recording-area").hide();

		if (videoRecordingPlayer) {
			videoRecordingPlayer.record().reset();
		}

		$("#tl-recording-audio-area").hide();

		if (audioRecordingPlayer) {
			audioRecordingPlayer.record().reset();
		}

		$('#assignment-reply-textbox-group').removeClass('visible-textbox').addClass('hidden-textbox');
		$('#documents-images-zip_namespace').hide();
		$('.tl-complete-button-assignment').hide();
		$('.tl-send-assignment-recording').addClass('disabled').hide();
		$('.tl-send-assignment-recording-audio').addClass('disabled').hide();
		$('.tl-send-assignment-recording-screen').addClass('disabled').show();
		$('.tl-assignment-select-method').parent().show();
		$('.tl-assignment-handles').hide();
		$("#tl-recording-screen-area").show();

		if (screenRecordingPlayer) {
			screenRecordingPlayer.record().getDevice();
		}
	});

    $(document).on('click', '.tl-assignment-modify-answer', function(){
		var replyType = $('#assignment-reply-type').text();
		$('#assignment-modify-answer-time').text(Math.floor(new Date().getTime()/1000));

		$('.tl-assignment-handles').show();
		$('.tl-pending-unit-handles').hide();
		$('.tl-incomplete-unit-handles').show();
		$('#documents-images-zip_namespace').hide();
		$('.tl-assignment-more-options-complete .tl-assignment-select-method').removeClass('tl-assignment-select-method').addClass('tl-assignment-cancel-modify').parent().show();
	});

    $(document).on('click', '.tl-assignment-cancel-modify', function(){
		$('.tl-assignment-handles').hide();
		$('.tl-pending-unit-handles').show();
		$('.tl-incomplete-unit-handles').hide();
		$("#tl-recording-area").hide();
		if(videoRecordingPlayer){
			videoRecordingPlayer.record().reset();
		}
		$("#tl-recording-audio-area").hide();
		if(audioRecordingPlayer){
			audioRecordingPlayer.record().reset();
		}
		$("#tl-recording-screen-area").hide();
		if(screenRecordingPlayer){
			screenRecordingPlayer.record().reset();
		}
		$('#documents-images-zip_namespace').hide();
		$('#assignment-reply-textbox-group').hide();
		$('#assignment-reply-textbox-group').removeClass('visible-textbox').addClass('hidden-textbox');
		$('.tl-complete-button-assignment').hide();
		$('.tl-send-assignment-recording').addClass('disabled').hide();
		$('.tl-send-assignment-recording-audio').addClass('disabled').hide();
		$('.tl-send-assignment-recording-screen').addClass('disabled').hide();
	});

    $(document).on('click', '.tl-assignment-check-answer', function(){
		var url = 'https://board.wincacademy.nl/unit/getassignmentreply/id:5194,mode:view';

		myportal.app.ajax(url, {
			type: 'GET',
			success: function(response){
				var data = myportal.app.parseResponse(response);
				var replyTypeFile = 'file';

				if(data.type == replyTypeFile && data.fileType != 'zip' && data.fileType != ''){
					$('#tl-assignment-check-answer-modal').addClass('preview-modal');
				}
				else{
					$('#tl-assignment-check-answer-modal').removeClass('preview-modal');
				}

				$('#tl-assignment-check-answer-modal .modal-body').html(data.reply);
				$('#tl-assignment-check-answer-modal .modal-header h3').html("Your answer");
				$('#tl-assignment-check-answer-modal').modal();
			}
		});
	});

    $(document).on('click', '.tl-assignment-checkreply', function(){
		var url = 'https://board.wincacademy.nl/unit/getassignmentreply/id:5194,mode:view';

		myportal.app.ajax(url, {
			type: 'GET',
			success: function(response){
				var data = myportal.app.parseResponse(response);

				$('#tl-assignment-check-answer-modal .modal-header h3').html("Instructor reply");
				$('#tl-assignment-check-answer-modal .modal-body').empty().append("<div style='margin-bottom: 7px;'><b>" + "Grade" + ":</b>&nbsp;" + data.grade + "</div>");
				$('#tl-assignment-check-answer-modal .modal-body').append("<div class='pull-left'><b>" + "Comments" + ":</b>&nbsp;</div><div class='pull-left' style='max-width:100%'>" + data.comments + "</div>");
				$('#tl-assignment-check-answer-modal').removeClass('preview-modal');
				$('#tl-assignment-check-answer-modal').modal();
			}
		});
	});

	$('#tl-assignment-check-answer-modal').bind('hidden', function(){	// empty modal on close so that videos/audio stop playing
		$('#tl-assignment-check-answer-modal .modal-body').html('');
	});

    $(document).on('click', '.tl-ilt-checkreply', function(){
		var url = 'https://board.wincacademy.nl/unit/getiltreply/id:5194';

		myportal.app.ajax(url, {
			type: 'GET',
			success: function(response){
				var data = myportal.app.parseResponse(response);

				$('#tl-ilt-check-answer-modal .modal-body').empty().append("<div style='margin-bottom: 7px;'><b>" + "Grade" + ":</b>&nbsp;" + data.grade + "</div>");
				$('#tl-ilt-check-answer-modal .modal-body').append("<div class='pull-left'><b>" + "Comments" + ":</b>&nbsp;</div><div class='pull-left'>" + data.comments + "</div>");
				$('#tl-ilt-check-answer-modal').modal();
			}
		});
	});

	$('.tl-failed-button-assignment').on('click', function(){
		var url = 'https://board.wincacademy.nl/unit/resetprogress/id:317723';
		myportal.app.ajax(url, {
			type: 'POST',
			data: {'myToken': myToken},
			success: function(){
				window.location = window.location.toString();
			}
		});
	});

	updateProgress = function(response){
		if(false && isLoggingOut){ // We bypass the parseResponse function in case of exception, since we do not want a pop-up when someone is logging out while in a SCORM file
			try{
				$.parseJSON(response);
			}
			catch (ex){
				console.log("Some error occurred");
				return;
			}
		}

		data = myportal.app.parseResponse(response);

		if(typeof(data) != 'undefined'){
			if(data.unit_status == 'completed'){	// means that the unit was completed
				if(data.progress_measure && $('#tl-navbar-progress-measure').length > 0){
					$('#tl-navbar-progress-measure').css('width', data.progress_measure + '%').text(data.progress_measure + '%');
					
					if (data.progress_measure == 100){
						$(".tl-courses-list").text('Go to course list');
						$(".tl-courses-list").removeAttr('data-dismiss');
						$(".tl-courses-list").attr('href', 'https://board.wincacademy.nl/dashboard/index');
					}
					
					if(data.course_completed){
						$('#tl-navbar-progress-measure').text("Completed");
					}
				}
				
				if(data.unit_id){
					if($('#tl-navbar-unit-link-' + data.unit_id).length > 0){
						$('#tl-navbar-unit-link-' + data.unit_id).css('fontWeight', 'bold');
						$('#tl-navbar-unit-link-' + data.unit_id).children('i').show();
					}
														
					var redirect_url = 'https://board.wincacademy.nl/unit/view/id:5202';
					window.location = redirect_url;
					return true;
								}

								$('.tl-incomplete-unit-handles').fadeOut('fast', function(){
					$('.tl-completed-unit-handles').fadeIn('fast');
					$('#tl-scorm-iframe-closed-message').find('h3').text("You have completed the unit");
				});
								
				if($('#tl-navbar-next-unit').length > 0){
					$('#tl-navbar-next-unit').attr('title', "Next");
					$('#tl-navbar-next-unit').children().removeClass('tl-disabled');
					$('#tl-navbar-next-unit').popover('destroy');
					$('#tl-navbar-next-unit').removeClass('tl-content-show-popover');
					
					if($('#tl-navbar-next-unit').attr('data-href') && $('#tl-navbar-next-unit').attr('data-href').length){
						$('#tl-navbar-next-unit').attr('href', $('#tl-navbar-next-unit').attr('data-href'));
					}
				}

				
				var gamificationPointsForUnitCompletion = $.cookie("gamification_points_for_unit_completion");
				var gamificationPointsForCourseCompletion = $.cookie("gamification_points_for_course_completion");
				var gamificationPointsForCertification = $.cookie("gamification_points_for_certification");
				var gamificationPointsNotification = '';
				var gamificationAddedPoints = 0;

				if(gamificationPointsForUnitCompletion){
					var parts = gamificationPointsForUnitCompletion.split('###');
					gamificationPointsNotification = parts[0];
					gamificationAddedPoints = parseInt(parts[1]);
					setTlmsCookie("gamification_points_for_unit_completion", null, {expires: -1, path: '/', domain: myEffectiveDomain, secure: false});
				}

				if(gamificationPointsForCourseCompletion){
					var parts = gamificationPointsForCourseCompletion.split('###');
					gamificationPointsNotification = (gamificationPointsNotification) ? gamificationPointsNotification + '<br/>' + parts[0] : parts[0];
					gamificationAddedPoints = gamificationAddedPoints + parseInt(parts[1]);
					setTlmsCookie("gamification_points_for_course_completion", null, {expires: -1, path: '/', domain: myEffectiveDomain, secure: false});
				}

				if(gamificationPointsForCertification){
					var parts = gamificationPointsForCertification.split('###');
					gamificationPointsNotification = (gamificationPointsNotification) ? gamificationPointsNotification + '<br/>' + parts[0] : parts[0];
					gamificationAddedPoints = gamificationAddedPoints + parseInt(parts[1]);
					setTlmsCookie("gamification_points_for_certification", null, {expires: -1, path: '/', domain: myEffectiveDomain, secure: false});
				}

				if(gamificationPointsNotification){
					if($("#tl-header-gamification-entrance").data('entrancemode') == 'points'){
						$("#tl-header-gamification-entrance").empty();
						var pointsCountUp = new countUp("tl-header-gamification-entrance", parseInt($("#tl-header-gamification-entrance").data('entrancevalue')), parseInt($("#tl-header-gamification-entrance").data('entrancevalue')) + parseInt(gamificationAddedPoints), 0, 1.5, {useEasing: true, useGrouping: true, separator: '', suffix: ' ' + "points"});
						pointsCountUp.start();
					}
					
					$("#tl-gamification-points-message").html(decodeURIComponent(gamificationPointsNotification)).fadeIn(1000);
					setTimeout(function(){$("#tl-gamification-points-message").fadeOut('slow');}, 3000);
				}

				var gamificationAssignmentBadge = $.cookie("gamification_assignment_badge");
				var gamificationLearningBadge = $.cookie("gamification_learning_badge");
				var gamificationCertificationBadge = $.cookie("gamification_certification_badge");
				var gamificationAddedBadges = 0;
				$(".tl-badge-image").attr('src', '');
				$(".tl-badge-message").empty();

				if(gamificationAssignmentBadge){
					var parts = gamificationAssignmentBadge.split('###');
					$(".tl-badge-image").attr('src', parts[1]);
					$(".tl-badge-message").html(decodeURIComponent(parts[0]));
					setTlmsCookie("gamification_assignment_badge", null, {expires: -1, path: '/', domain: myEffectiveDomain, secure: false});
					gamificationAddedBadges++;
				}

				if(gamificationLearningBadge){
					var parts = gamificationLearningBadge.split('###');
					setTlmsCookie("gamification_learning_badge", null, {expires: -1, path: '/', domain: myEffectiveDomain, secure: false});
					gamificationAddedBadges++;

					if($(".tl-badge-image").attr('src') != '' && $(".tl-badge-message").html() != ''){
						$("#tl-gamification-badges-message").append('<hr/><div id="learning-badge-message" class="tl-badge-image-message-wrapper"></div>');
						$("#learning-badge-message").append('<img class="tl-badge-image pull-left image60x60" src="' + parts[1] + '"/>').append('<div class="tl-badge-message text-center tl-bold-item">' + decodeURIComponent(parts[0]) + '</div>');
					}
					else{
						$(".tl-badge-image").attr('src', parts[1]);
						$(".tl-badge-message").html(decodeURIComponent(parts[0]));
					}
				}

				if(gamificationCertificationBadge){
					var parts = gamificationCertificationBadge.split('###');
					setTlmsCookie("gamification_certification_badge", null, {expires: -1, path: '/', domain: myEffectiveDomain, secure: false});
					gamificationAddedBadges++;

					if($(".tl-badge-image").attr('src') != '' && $(".tl-badge-message").html() != ''){
						$("#tl-gamification-badges-message").append('<hr/><div id="certification-badge-message" class="tl-badge-image-message-wrapper"></div>');
						$("#certification-badge-message").append('<img class="tl-badge-image pull-left image60x60" src="' + parts[1] + '"/>').append('<div class="tl-badge-message text-center tl-bold-item">' + decodeURIComponent(parts[0]) + '</div>');
					}
					else{
						$(".tl-badge-image").attr('src', parts[1]);
						$(".tl-badge-message").html(decodeURIComponent(parts[0]));
					}
				}

				if(gamificationAssignmentBadge || gamificationLearningBadge || gamificationCertificationBadge){
					if(gamificationPointsNotification){
						$("#tl-gamification-badges-message").css('bottom', $("#tl-gamification-points-message").height() + 20 + 16 + 5);
					}

					if($("#tl-header-gamification-entrance").data('entrancemode') == 'badges'){
						$("#tl-header-gamification-entrance").empty();
						var badgesCountUp = new countUp("tl-header-gamification-entrance", 0, parseInt($("#tl-header-gamification-entrance").data('entrancevalue')) + parseInt(gamificationAddedBadges), 0, 1.5, {useEasing: true, useGrouping: true, separator: '', suffix: ' ' + "badges"});
						badgesCountUp.start();
					}

					$("#tl-gamification-badges-message").fadeIn(1000).css('display', 'table');
					setTimeout(function(){$("#tl-gamification-badges-message").fadeOut('slow');}, 5000);
				}

				var gamificationCompletedCourses = $.cookie("gamification_completed_courses");

				if(gamificationCompletedCourses && ($("#tl-header-gamification-entrance").data('entrancemode') == 'courses' || $("#tl-header-gamification-entrance").data('entrancemode') == 'certifications')){
					$("#tl-header-gamification-entrance").empty();
					var completedCoursesCountUp = new countUp("tl-header-gamification-entrance", 0, parseInt(gamificationCompletedCourses), 0, 1.5, {useEasing: true, useGrouping: true, separator: '', suffix: ' ' + "completed courses"});
					completedCoursesCountUp.start();
					setTlmsCookie("gamification_completed_courses", null, {expires: -1, path: '/', domain: myEffectiveDomain, secure: false});
				}

				var gamificationUserLevel = $.cookie("gamification_user_level");

				if(gamificationUserLevel && $("#tl-header-gamification-entrance").data('entrancemode') == 'levels'){
					var gamificationUserLevelParts = gamificationUserLevel.split('###');
					$("#tl-header-gamification-entrance").empty();
					var userLevelCountUp = new countUp("tl-header-gamification-entrance", 0, parseInt(gamificationUserLevelParts[0]), 0, 1.5, {useEasing: true, useGrouping: true, separator: ''});
					userLevelCountUp.start(function(){$('#tl-header-gamification-entrance').html(decodeURIComponent(gamificationUserLevelParts[1]));});
					setTlmsCookie("gamification_user_level", null, {expires: -1, path: '/', domain: myEffectiveDomain, secure: false});
				}
			}
			else if(data.unit_status == 'pending'){	// means that the unit is in a pending status now (assignment units)
				
				$('.tl-incomplete-unit-handles').fadeOut('fast', function(){
					$('.tl-pending-unit-handles').fadeIn('fast');
				});
				$('#tl-recording-area').fadeOut('fast');
				$('#tl-recording-audio-area').fadeOut('fast');
				$('#tl-recording-screen-area').fadeOut('fast');
			}
			else{
				
				$('#tl-submit-question').removeClass('disabled').addClass('btn-danger').text("Incorrect answer, try again");
				setTimeout(function(){
					$('#tl-submit-question').fadeOut('slow', function(){
						$('#tl-submit-question').removeClass('btn-danger').text("Submit answer");
						$('#tl-submit-question').fadeIn(400);
					});}, 2000);

							}
		}	
	}
	
	submitResults = function(url){
		myportal.app.ajax(url, {
			type: 'post',
			data: $('.tl-unit-question-form').serialize() + "&myToken=" + myToken,
			success: function(response){
				updateProgress(response);
			},
			error: function(jqXHR_obj){
				var response = $.parseJSON(jqXHR_obj.responseText);
				$('#tl-submit-question').removeClass('disabled');
				myportal.app.notify({type: "error", message: decodeURIComponent(response.message)});
			}
		});
	}

	window.completeUnit = function(el){
		var url = $(el).attr('data-toggle');
		if(typeof(url) != 'undefined'){
			myportal.app.ajax(url, {
				type: 'GET',
				success: function(response){
										$('#last-unit-progress').text('');
					
					updateProgress(response);
				},
				error: function(jqXHR_obj){
					var response = $.parseJSON(jqXHR_obj.responseText);
					myportal.app.notify({type: "error", message: decodeURIComponent(response.message)});
				}
			});
		}
	}

	completeAssignmentUnit = function(el, fileId){
		var assignmentId = '5194';
		var replyType = '';
		var url = '';

		if(el == null && fileId != null){
			url = 'https://board.wincacademy.nl/unit/complete';
		}
		else{
			url = $(el).attr('data-toggle');
		}

		if($('#assignment-reply-textbox-group').hasClass('hidden-textbox')){
			replyType = 'file';
		}
		else{
			replyType = 'textbox';
		}

		$('#assignment-reply-type').text(replyType);

		if(typeof(url) != 'undefined'){
			myportal.app.ajax(url, {
				type: 'POST',
				data: {'id': assignmentId, 'textbox-reply': $('#assignment-reply-textbox').val(), 'reply-type': replyType, 'reply-file': fileId, 'assignment-modify-answer-time': $('#assignment-modify-answer-time').text()},
				success: function(response){
										$('#last-unit-progress').text('');
					
					updateProgress(response);
					$('.tl-complete-button-assignment').text("Send your reply").removeClass('disabled');
					if($('#assignment-reply-textbox-group').hasClass('visible-textbox')){
						$('#assignment-reply-textbox-group').removeClass('visible-textbox').addClass('hidden-textbox');
						$('#assignment-reply-textbox-group').fadeOut('slow');
						$('.tl-complete-button-assignment').hide();
					}
				}
			});
		}
	}

		$('#tl-submit-question').on('click', function(){
		if($(this).hasClass('disabled') || $(this).hasClass('btn-success') || $(this).hasClass('btn-danger')){
			return false;
		}

		$(this).addClass('disabled');
		var url = 'https://board.wincacademy.nl/unit/submitquestion/id:5194,questionId:,questionType:';
		submitResults(url);
	});
	
    $(document).on('click', '.tl-complete-button, .tl-complete-button-assignment', function(){
		if($(this).hasClass('disabled')){
			return;
		}

				$(this).text("Completing...").addClass('disabled');
		
		if(!$(this).hasClass('tl-complete-button-assignment')){
			completeUnit($(this));
		}
		else{
			$('#assignment-reply-textbox').val($('.tl-assignment-reply-editor').code());
			completeAssignmentUnit($(this), null);
		}
	});

	$(document).on('click', '.tl-send-assignment-recording', function(){
		if($(this).hasClass('disabled') || !recordedData){
			return;
		}

		// Videos shorter than 5 seconds seem to have issues in EncodeMagic. Check the duration (written in the recorder's toolbar) and if too small do nothing
		var parts = $('#tl-recording-video span.vjs-duration-display').text().split(':');
		if(parts.length == 2){
			if(parts[0]*60+parts[1]*1 < 6){ // multiply seconds with 1 to be sure we have an integer and not a string
				$('#tl-record-error').text('Video should be longer than 5 seconds').removeClass('hide');
				$('.tl-send-assignment-recording').addClass('disabled');
				return;
			}
		}
		else if(parts.length == 3){
			if(parts[0]*3600+parts[1]*60+parts[2]*1 < 6){ // multiply seconds with 1 to be sure we have an integer and not a string
				$('#tl-record-error').text('Video should be longer than 5 seconds').removeClass('hide');
				$('.tl-send-assignment-recording').addClass('disabled');
				return;
			}
		}

		var uploadUrl = 'https://board.wincacademy.nl/unit/uploadassignmentreply/id:5194';
		var _formData = new FormData();
		_formData.append('files', recordedData, recordedData.name);

		myportal.app.ajax(uploadUrl,{
			type: "POST",
			data: _formData,
			cache: false,
			dataType: 'json',
			processData: false,
			contentType: false,
			success: function(resp){
				if(resp.success){
					$('.tl-send-assignment-recording').addClass('disabled').hide();
					completeAssignmentUnit(null, resp.data.assignmentReplyFile);
				}
			}
		});
	});

	$(document).on('click', '.tl-send-assignment-recording-audio', function(){
		if($(this).hasClass('disabled') || !recordedAudioData){
			return;
		}

		// Videos/audio shorter than 5 seconds seem to have issues in EncodeMagic. Check the duration (written in the recorder's toolbar) and if too small do nothing
		var parts = $('#tl-recording-audio span.vjs-duration-display').text().split(':');

		if(parts.length == 2){
			if(parts[0]*60+parts[1]*1 < 6){ // multiply seconds with 1 to be sure we have an integer and not a string
				$('#tl-record-audio-error').text('Audio should be longer than 5 seconds').removeClass('hide');
				$('.tl-send-assignment-recording-audio').addClass('disabled');
				return;
			}
		}
		else if(parts.length == 3){
			if(parts[0]*3600+parts[1]*60+parts[2]*1 < 6){ // multiply seconds with 1 to be sure we have an integer and not a string
				$('#tl-record-audio-error').text('Audio should be longer than 5 seconds').removeClass('hide');
				$('.tl-send-assignment-recording-audio').addClass('disabled');
				return;
			}
		}

		var uploadUrl = 'https://board.wincacademy.nl/unit/uploadassignmentreply/id:5194';
		var _formData = new FormData();
		_formData.append('files', recordedAudioData, recordedAudioData.name);

		myportal.app.ajax(uploadUrl,{
			type: "POST",
			data: _formData,
			cache: false,
			dataType: 'json',
			processData: false,
			contentType: false,
			success: function(resp){
				if(resp.success){
					$('.tl-send-assignment-recording-audio').addClass('disabled').hide();
					completeAssignmentUnit(null, resp.data.assignmentReplyFile);
				}
			}
		});
	});

	$(document).on('click', '.tl-send-assignment-recording-screen', function() {
		if ($(this).hasClass('disabled') || !recordedScreenData) {
			return;
		}

		// Videos shorter than 5 seconds seem to have issues in EncodeMagic. Check the duration (written in the recorder's toolbar) and if too small do nothing
		var parts = $('#tl-screen-recording span.vjs-duration-display').text().split(':');
		if (parts.length === 2) {
			if (parts[0]*60+parts[1]*1 < 6) { // multiply seconds with 1 to be sure we have an integer and not a string
				$('#tl-screen-record-error').text('Video should be longer than 5 seconds').removeClass('hide');
				$('.tl-send-assignment-recording-screen').addClass('disabled');
				return;
			}
		} else if (parts.length === 3) {
			if (parts[0]*3600+parts[1]*60+parts[2]*1 < 6) { // multiply seconds with 1 to be sure we have an integer and not a string
				$('#tl-screen-record-error').text('Video should be longer than 5 seconds').removeClass('hide');
				$('.tl-send-assignment-recording-screen').addClass('disabled');
				return;
			}
		}

		var uploadUrl = 'https://board.wincacademy.nl/unit/uploadassignmentreply/id:5194';
		var _formData = new FormData();
		_formData.append('files', recordedScreenData, recordedScreenData.name);

		myportal.app.ajax(uploadUrl, {
			type: "POST",
			data: _formData,
			cache: false,
			dataType: 'json',
			processData: false,
			contentType: false,
			success: function(resp) {
				if (resp.success) {
					$('.tl-send-assignment-recording-screen').addClass('disabled').hide();
					completeAssignmentUnit(null, resp.data.assignmentReplyFile);
				}
			}
		});
	});

		
	$('.tl-scorm-frame').ready(function(){		
		$('#tl-scorm-progress-bar').hide();
		$('.tl-complete-button-scorm').show().removeClass('disabled').text("Incomplete").popover({'placement': 'top', 'html': true, content: "This unit will be auto-completed when its completion conditions are met. In case you want to force exit and check for completion status click <a href='javascript:void(0)' class='tl-complete-button-scorm-link'><strong>here</strong></a>."});

		$(document).on('click', '.tl-complete-button-scorm-link', function(){
			$('.tl-complete-button-scorm').popover('destroy');
			$('.tl-scorm-frame').attr('src', '').remove(); // .remove() without emptying the iframe content, sometimes crashes ie
			$('.tl-complete-button-scorm').hide().text("Incomplete. Click to retry.").on('click', function() {window.location.reload()}).fadeIn('slow');
			$('#tl-scorm-iframe-closed-message').fadeIn('slow');		
		});
	});
	
	$('#tl-reset-progress').on('click', function(){
		if(tl_timer_id){
			tl_stopTimer(start_time);
		}

		var lastUnitProgress = $('#last-unit-progress').text();

		if(lastUnitProgress != ''){
			var url = 'https://board.wincacademy.nl/unit/resetprogress/id:##unit_progress_id##'.replace('##unit_progress_id##', lastUnitProgress);
		}
		else{
			var url = 'https://board.wincacademy.nl/unit/resetprogress/id:317723';
		}

		myportal.app.ajax(url, {
			type: 'POST',
			data: {'myToken': myToken},
			success: function(){
								$('.tl-completed-unit-handles').fadeOut('fast', function(){
					$('.tl-incomplete-unit-handles').fadeIn('fast');

					
					if(window.clearQuestion){
						window.clearQuestion();		// Clear the question's results
					}

					isCompleted = false;

					if(parseInt(start_time) > 0){
						tl_initTimerValue(start_time);
						tl_setUpCounter(start_time);
					}

					$('#tl-submit-question').removeClass('btn-danger').removeClass('btn-success').text("Submit answer").show();
					$('.tl-question-preview-feedback').css('display', 'none');

									});
							}
		});
	});

	window.start_time = '0';

	window.tl_setUpCounter = function (secondsFromNow){
		if(tl_timer_id){
			tl_stopTimer(secondsFromNow);
		}

		setUnitEndDate(parseInt(secondsFromNow));
		tl_timer_id = window.setInterval(tl_startCounter, 300);
	};

	window.tl_startCounter = function (){
		var currentDate = new Date();
		var restOfSeconds = Math.ceil((unitEndDate.getTime() - currentDate.getTime()) / 1000);

		if(restOfSeconds > 0){
			$('#tl-timer-seconds').text(restOfSeconds);
			var interval = formatTimeInterval(restOfSeconds);

			if(!interval){
				$('.tl-timer-button').text("Ready!");
			}
			else{
				$('#tl-timer').text(interval);
			}
		}
		else {
			tl_stopTimer(start_time);
			tl_completeUnit();
		}
	}

    window.formatTimeInterval = function(interval){
    	var seconds = interval % 60;
    	var minutes = ((interval - seconds) / 60) % 60;
    	var hours = ((interval - seconds - (minutes * 60)) / 3600) % 24;
    	var days = (interval - hours * 3600 + minutes * 60 + seconds) / (24 * 3600);
    	var str = new Array();

    	if(days >= 1){
    		str.push("###days###d".replace('###days###', parseInt(days)));
    	}

    	if(hours){
    		str.push("###hours###h".replace('###hours###', hours));
    	}

    	if(minutes){
    		str.push("###minutes###m".replace('###minutes###', minutes));
    	}

    	if(seconds){
    		str.push("###seconds###s".replace('###seconds###', seconds));
    	}

    	return str.join(' ');
    }

	/**
	 * Sets the date that the unit will end.
	 * @param {*} secondsFromNow
	 */
	window.setUnitEndDate = function(secondsFromNow){
		if(secondsFromNow === false) {
			secondsFromNow = start_time;
		}

		unitEndDate = new Date();
		unitEndDate.setSeconds(unitEndDate.getSeconds() + parseInt(secondsFromNow));
	};

	
		if (typeof window.syncVideoUnitTimer === 'undefined' || !window.syncVideoUnitTimer){
		if(!tl_timer_id){
			tl_setUpCounter(start_time);
		}
	}
	else {
		tl_timer_id = null;
	}
	
		$(window).on('DOMContentLoaded', function(){
		$.ajax('https://board.wincacademy.nl/unit/enter/id:317723', {async: false});
	});

			$(window).on('beforeunload', function(){
						if('fetch' in window){
				fetch('https://board.wincacademy.nl/unit/exit/id:317723', {keepalive: true});
			}
			else{
				$.ajax('https://board.wincacademy.nl/unit/exit/id:317723', {async: false});
			}
					});
	
	});


function tl_initTimerValue(time){
	time = parseInt(time);
	buttonText = "Completes in <span id = 'tl-timer'>%s</span>";

	if (time < 1){
		time = 1;
	}

	start_time = time;
	$('#tl-timer-seconds').text(time);
	interval = formatTimeInterval(time);

	if(interval){
		$('.tl-timer-button').html(buttonText.replace('%s', interval));
	}
}

function tl_startTimer(){
	if(tl_timer_id){
		tl_stopTimer($('#tl-timer-seconds').text());
	}

	tl_setUpCounter($('#tl-timer-seconds').text());
}

function tl_stopTimer(time){
	window.clearInterval(tl_timer_id);
	tl_timer_id = false;
	time = parseInt(time);
	cur_time = parseInt($('#tl-timer-seconds').text());
	if (time < 1){
		time = 1;
	}
	if(cur_time < time ) {
		return;
	}
	$('#tl-timer-seconds').text(time - 1);
	interval = formatTimeInterval(time - 1);

	if(!interval){
		$('.tl-timer-button').text("Ready!");
	}
	else{
		$('#tl-timer').text(interval);
	}
}
function tl_completeUnit(){
	completeUnit($('.tl-timer-button'));
}


var heartbeatInterval = 10790*1000; setInterval(function(){
	myportal.app.ajax("https://board.wincacademy.nl/index/heartbeat", {
		'type': 'GET'
	});
}, heartbeatInterval);


</script>			</div>
