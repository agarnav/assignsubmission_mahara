assignsubmission-mahara
============================

Mahara assignment submission plugin for Moodle 2.3+

This plugin adds Mahara pages submission functionality to assignments in
Moodle. Plugin works with the new assignment type introduced in 2.3. It
requres to have at least one Mahara site linked to Moodle.

The plugin has funtionality of old Mahara submission type plugin
(https://gitorious.org/mahara-contrib/mod-assignment-type-mahara) with some imporvements. In particular:

* graded page will never become editable again,
* the same page cannot be submitted more than once,
* the page used in the draft submission is not locked for editing in Mahara, but not avialable for being used in different submission.

The plugin also allows exporting old Mahara submission assignments to the assignments of new type. The plugin does not include featues to communicate with outcomes artefact plugin.

Logic
-----

If user is required to click submit button to declare submission is final (defined in assignment settings):
On submission, the submitted Page will be locked in Mahara and submission editing will not be possible in Moodle. To make an edit, teacher should release submission to draft. The same way it works for any submission type (file or onlinetext).

If user is NOT required to click submit button to declare submission is final (defined in assignment settings):
On submission, the submitted Page will be locked in Mahara and submission editing will not be possible in Moodle.

Once the Page is submitted for assesment and graded, it will never become editable in Mahara any more. The same happens if extra attempt is given in Moodle 2.5 - already submitted page will never be released in Mahara. User is still able to make a copy of locked page in Mahara, and use it in the second attempt of submission, which is useful in case when some amendment is required.

Installation
------------
1. Make sure that your Moodle version is up-to-date (recent update included
   assign mod chnages required for this plugin).
2. Copy the content to mod/assign/submission/mahara
3. Proceed with installation in Moodle.
4. In Site Admin > Networking > Peers choose the Mahara one, open Services
      tab and enable Assign Submission Mahara services.
5. Now you may create your first Mahara assignment.
