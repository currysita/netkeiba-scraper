netkeiba-scraper ��fork���ĉ��ǂ��Ă݂܂����B

#�I���W�i���Ƃ̑���_
- build.sbt �̏C��
-- scala-xml ��ǉ��B�͕̂W���Ŋ܂܂�Ă������ł��B
-- scalikejdbc �̃o�[�W������ 2.5.2 �ɂ��܂����B�擾���鎞�ɃG���[���o�Ă����̂ŁAURL�𒼐ڊJ���Ďg�p�\�ȃo�[�W������T���܂����B
- URL�̕ύX
-- http��URL���p�~����Ă���̂ŁAhttps�ɕύX���܂����B
- sbt.bat���C��
-- sbtconfig.txt ��������Ȃ��x�����o�Ă��̂ɑΏ����܂����B���|�W�g������ sbtconfig.txt ���܂߂Ă����ǂނ悤�ɂ��܂����B
- sbtconfig.txt �̓��e
-- xmx��1024M�ɐݒ�B�����PC�Ȃ�قڑ��v�ł��傤�B�኱���x�����P���܂����B
- �e�[�u���̍\�����C��
-- �n�̖��O���擾����悤�C�����܂����B
-- �^�C���������񂵂��Ȃ������̂ŁAreal�^�̕b���Ƃ��Ď擾����悤�ɂ��܂����B
- ���̑�
-- �����ȃ��[�X����ǉ����܂����B

�ȉ��̓I���W�i���� README.md �̓��e�ł��B

#�g����
�ȉ��̃R�}���h���ォ�珇�Ɏ��s���Ă����΍Ō�ɑf�����쐬�����B
```
sbt "run collecturl"
```
���[�X���ʂ��ڂ��Ă���URL�����W���āurace_list.txt�v�ɕۑ�����B
```
sbt "run scrapehtml"
```
���[�X���ʂ�HTML���X�N���C�s���O����html�t�H���_�ɕۑ�����BHTML���܂邲�ƃX�N���C�s���O����̂Ō��\���Ԃ�������B
```
sbt "run extract"
```
HTML���烌�[�X���ʂ𔲂��o��SQLite�ɕۑ�����B
```
sbt "run genfeature"
```
���[�X���ʂ����ɂ��đf�������SQLite�ɕۑ�����B