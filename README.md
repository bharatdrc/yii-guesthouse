# yii-guesthouse

################ADD CONSTANT###################
\TYPO3\CMS\Core\Utility\ExtensionManagementUtility::addTypoScript('site_config', 'constants', '<INCLUDE_TYPOSCRIPT: source="FILE:EXT:'.$_EXTKEY.'/Configuration/TypoScript/Constant/constant.txt">');

#############PRINT QUERY 8.7############
$queryParser = $this->objectManager->get(\TYPO3\CMS\Extbase\Persistence\Generic\Storage\Typo3DbQueryParser::class);
 \TYPO3\CMS\Extbase\Utility\DebuggerUtility::var_dump($queryParser->convertQueryToDoctrineQueryBuilder($query)->getSQL());
 \TYPO3\CMS\Extbase\Utility\DebuggerUtility::var_dump($queryParser->convertQueryToDoctrineQueryBuilder($query)->getParameters());
 ################################################################3
 
 https://blogs.msdn.microsoft.com/bethmassi/2011/02/09/how-to-send-automated-appointments-from-a-lightswitch-application/
sudo FLOW_CONTEXT=Development/Application ./flow mt:createevent
sudo FLOW_CONTEXT=Development/Application ./flow doctrine:migrate
sudo FLOW_CONTEXT=Development/Application ./flow doctrine:validate
sudo FLOW_CONTEXT=Development/Application ./flow flow:doctrine:update
sudo FLOW_CONTEXT=Development/Application ./flow mt:importstatic
 activateevent:sendremaindermail
sudo FLOW_CONTEXT=Development/Application ./flow mt:createuseraccount
sudo FLOW_CONTEXT=Development/Application ./flow configuration:validate
sudo FLOW_CONTEXT=Development/Application ./flow flow:cache:flush
sudo FLOW_CONTEXT=Development/Application ./flow flow:security:showeffectivepolicy
sudo FLOW_CONTEXT=Development/Application ./flow flow:security:showmethodsforprivilegetarget

sudo FLOW_CONTEXT=Development/Application ./flow security:showunprotectedactions
sudo FLOW_CONTEXT=Development/Application ./flow core:migrate --package-key MeetingTool.Portal
###############################################################################################################
ssh -i /home/drc/id_rsa root@domain
#############################################################################################################
function loadTS($pageUid) {
      $backendUtility = \TYPO3\CMS\Core\Utility\GeneralUtility::makeInstance('TYPO3\\CMS\\Backend\\Utility\\BackendUtility');
      $rootLine = $backendUtility->BEgetRootline($pageUid);
      $TSObj = \TYPO3\CMS\Core\Utility\GeneralUtility::makeInstance('TYPO3\\CMS\\Core\\TypoScript\\TemplateService');
      $TSObj->tt_track = 0;
      $TSObj->init();
      $TSObj->runThroughTemplates($rootLine);
      $TSObj->generateConfig();
      return $TSObj->setup['config.']['baseURL'];
  }
######################TYPOscript assign object################################
<f:cObject typoscriptObjectPath="menu.content" data="{a:'3'}" />

    special = directory
    special.value.cObject < lib.pidvalue
#######################################TYposcript check POST value#######################
[globalVar = _POST|tx_powermail_pi1|field|newsletter|0 = newsletter]
#########################Slow Span in rte and wrap it##########################
RTE.default.contentCSS = fileadmin/RTE/rte.css   # here I create the rte.css file and insert 2 classes (.price1 and .price2)

RTE.default.buttons.textstyle.showTagFreeClasses = 1
RTE.default.buttons.blockstyle.showTagFreeClasses = 1

RTE.default.proc.allowedClasses := addToList(price1, price2)
RTE.classes {
price1.name = Preis Gross
price1.value = background-color: #fff; color: #333;
}
RTE.classes {
price2.name = Preis klein
price1.value = background-color: #fff; color: #333;
}

RTE.default.buttons {
 textstyle.tags.span.allowedClasses  := addToList(price1, price2)
}
RTE.default.FE < RTE.default

###################################################################

##################################################PHP 5.6 and 7.1###########
apt-get dist-upgrade


>sudo add-apt-repository ppa:ondrej/php
>sudo apt-get update
>sudo apt-get install php7.0 php5.6 php5.6-mysql php-gettext php5.6-mbstring php-mbstring php7.0-mbstring php-xdebug libapache2-mod-php5.6 libapache2-mod-php7.0
>sudo apt install php libapache2-mod-php
>sudo apt install php7.0-mbstring

2. Switch PHP version:

From php5 to php7.0 :
  Apache:
  sudo a2dismod php5 ; sudo a2enmod php7.1 ; sudo service apache2 restart
  CLI:
  sudo update-alternatives --set php /usr/bin/php7.1
From php7.1 to php5.6 :
  Apache:
  sudo a2dismod php7.1 ; sudo a2enmod php5 ; sudo service apache2 restart
  CLI:
  sudo update-alternatives --set php /usr/bin/php5



#######################################################################


sudo service apache2 restart

#############################Virtual Host##########################3
$ cd /etc/apache2/sites-available/
$ sudo cp 000-default.conf event2.localhost.com.conf
$ vim site1.example.com.conf
<VirtualHost *:80>
        ServerAdmin webmaster@event2.localhost.com
        ServerName event2.localhost.com
        DocumentRoot /var/www/html/foldername
</VirtualHost>
$ a2ensite event2.localhost.com ==>include new file on load
$ service apache2 reload
cd /etc/
vim hosts
192.168.1.100  site1.example.com ==>in host file
###################################################################3

#####################################################
 if (!(@is_dir($destinationFolder) || @mkdir($destinationFolder, 0777, true))) {
######################################

If Error of user rights :
git clone [http link]
git branch
sudo service apache2 restart|stop|start
git checkout -b [new branch]

	1) exec ssh-agent bash
	2) ssh-add ../id_rsa
	 exec ssh-agent bash
     ssh-add ../../../id_rsa

composer create-project --no-dev --prefer-source

'installToolPassword' => '$1$ZPhMgX9v$vxgBRXrQtseNQq6CfqAZ31',
GIT Commit Commands :
1) git checkout -b final origin/master
2) ==> git status
3) git config core.fileMode false
5) git add .(sudo chmod 777 -R .git/objects)
6) git commit -a // git commit -a --amend
7) git push origin HEAD:refs/for/master // git push -u origin master
############################################################################

t3lib_div::debug($out);exit;
\TYPO3\CMS\Extbase\Utility\LocalizationUtility::translate('tx_petitie_domain_model_counter.first_name','petitie')

 \TYPO3\CMS\Extbase\Utility\DebuggerUtility::var_dump($);exit;
\TYPO3\CMS\Core\Utility\DebugUtility::debug($this->request->getArguments());exit;

#########################LIGHTBOX CLASS##############################
lib.contentElement.variables.10 = LOAD_REGISTER
lib.contentElement.variables.10.content_uid = TEXT
lib.contentElement.variables.10.content_uid.field = uid
lib.contentElement.settings.media.popup.linkParams.ATagParams.dataWrap = class="lightbox" data-fancybox-group="lightbox{register:content_uid}"
lib.contentElement.stdWrap.append = RESTORE_REGISTER
#############################################################################
###########################################TRANSLATE###########################
\TYPO3\CMS\Extbase\Utility\LocalizationUtility::translate('Label.mailSent','sail_offer')
<f:translate id="Label.addCompany" />
{f:translate(id:'Label.save')}


#################################################################################
#################################Header image######################
page.footerData {
  10 = FILES
  10 {
     references.data =  levelmedia:-1, slide
     references.listNum = 0
     renderObj = TEXT
     renderObj.data = file:current:publicUrl

     renderObj.wrap (
     .title-1 {
        background-image: url(../|);
      }
    )
  }
}
####################################################################

###################################################################3
$configurationManager = \t3lib_div::makeInstance('Tx_Extbase_Configuration_ConfigurationManager');

    $this->settings = $configurationManager->getConfiguration(\TYPO3\CMS\Extbase\Configuration\ConfigurationManagerInterface::CONFIGURATION_TYPE_SETTINGS,'typo3forum','pi1');

########################################Debug#################################

