---
description: 'Дополнительные сведения о: Есентобсолетиксцептион Class'
title: Класс EsentObsoleteException
TOCTitle: EsentObsoleteException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentObsoleteException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102357
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: db67425defce2b2247aa7ba94a9742c53a671c27287d76474223cbc050725f5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118494021"
---
# <a name="esentobsoleteexception-class"></a>Класс EsentObsoleteException

Базовый класс для устаревших исключений.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентапиексцептион](./esentapiexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион  
            

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentObsoleteException _
    Inherits EsentApiException
'Usage
Dim instance As EsentObsoleteException
```

``` csharp
[SerializableAttribute]
public abstract class EsentObsoleteException : EsentApiException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Элементы Есентобсолетиксцептион](./esentobsoleteexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Производные типы

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентапиексцептион](./esentapiexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион  
            [Microsoft. ISAM. ESENT. Interop. Есентакцессдениедексцептион](./esentaccessdeniedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентбадбаккупдатабасесизиксцептион](./esentbadbackupdatabasesizeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентбадбукмаркексцептион](./esentbadbookmarkexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентбаддбсигнатуриксцептион](./esentbaddbsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентбадпатчпажеексцептион](./esentbadpatchpageexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентбадслвсигнатуриксцептион](./esentbadslvsignatureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентканнотаддфикседварколумнтодериведтабликсцептион](./esentcannotaddfixedvarcolumntoderivedtableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентканнотнестдистрибутедтрансактионсексцептион](./esentcannotnestdistributedtransactionsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентколумниндекседексцептион](./esentcolumnindexedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентколумнинрелатионшипексцептион](./esentcolumninrelationshipexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентколумнлонжексцептион](./esentcolumnlongexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентконтаинернотемптексцептион](./esentcontainernotemptyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенткурренцистаккаутофмеморексцептион](./esentcurrencystackoutofmemoryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabase200FormatException](./esentdatabase200formatexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabase400FormatException](./esentdatabase400formatexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentDatabase500FormatException](./esentdatabase500formatexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдатабасеидинусиксцептион](./esentdatabaseidinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдатабасепатчфилемисматчексцептион](./esentdatabasepatchfilemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдатабасеснотфромсамеснапшотексцептион](./esentdatabasesnotfromsamesnapshotexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдатабасестреамингфилемисматчексцептион](./esentdatabasestreamingfilemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдатабасеунаваилабликсцептион](./esentdatabaseunavailableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдатахасчанжедексцептион](./esentdatahaschangedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдистрибутедтрансактионалреадипрепаредтокоммитексцептион](./esentdistributedtransactionalreadypreparedtocommitexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдистрибутедтрансактионнотетпрепаредтокоммитексцептион](./esentdistributedtransactionnotyetpreparedtocommitexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдтккаллбаккунекспектедеррорексцептион](./esentdtccallbackunexpectederrorexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдткмиссингкаллбаккексцептион](./esentdtcmissingcallbackexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдткмиссингкаллбакконрековерексцептион](./esentdtcmissingcallbackonrecoveryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентфилеклосиксцептион](./esentfilecloseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентфилеиоабортексцептион](./esentfileioabortexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентфилеиофаилексцептион](./esentfileiofailexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентфилеиоретрексцептион](./esentfileioretryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентфилеиоспарсиксцептион](./esentfileiosparseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентиндекскантбуилдексцептион](./esentindexcantbuildexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентиндекступлестуманиколумнсексцептион](./esentindextuplestoomanycolumnsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентинвалидкаунтрексцептион](./esentinvalidcountryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентинвалидфиленамиксцептион](./esentinvalidfilenameexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентинвалидлогдиректорексцептион](./esentinvalidlogdirectoryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентинвалидлогжедоператионексцептион](./esentinvalidloggedoperationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентинвалидобжектексцептион](./esentinvalidobjectexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентинвалидонсортексцептион](./esentinvalidonsortexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентинвалидсистемпасексцептион](./esentinvalidsystempathexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенткэйбаундарексцептион](./esentkeyboundaryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенткэйтубижексцептион](./esentkeytoobigexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлангуаженотсуппортедексцептион](./esentlanguagenotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлинкнотсуппортедексцептион](./esentlinknotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлогбуффертусмаллексцептион](./esentlogbuffertoosmallexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентмиссингпатчпажеексцептион](./esentmissingpatchpageexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentMustCommitDistributedTransactionToLevel0Exception](./esentmustcommitdistributedtransactiontolevel0exception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентмустдисаблелоггингфордбупградиксцептион](./esentmustdisableloggingfordbupgradeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентнотиндистрибутедтрансактионексцептион](./esentnotindistributedtransactionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентобжектдупликатиксцептион](./esentobjectduplicateexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентпажебаундарексцептион](./esentpageboundaryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентпатчфилемиссинжексцептион](./esentpatchfilemissingexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентрфсфаилуриксцептион](./esentrfsfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентрфснотармедексцептион](./esentrfsnotarmedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентроллбаккрекуиредексцептион](./esentrollbackrequiredexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвбуффертусмаллексцептион](./esentslvbuffertoosmallexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвколумнканнотделетиксцептион](./esentslvcolumncannotdeleteexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвколумндефаултвалуеноталловедексцептион](./esentslvcolumndefaultvaluenotallowedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвкорруптедексцептион](./esentslvcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвдатабасемиссинжексцептион](./esentslvdatabasemissingexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвеалисткорруптексцептион](./esentslvealistcorruptexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвеалисттубижексцептион](./esentslvealisttoobigexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвеалистзероаллокатионексцептион](./esentslvealistzeroallocationexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвфилеакцессдениедексцептион](./esentslvfileaccessdeniedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвфилеинусиксцептион](./esentslvfileinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвфилеинвалидпасексцептион](./esentslvfileinvalidpathexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвфилеиоексцептион](./esentslvfileioexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвфиленотфаундексцептион](./esentslvfilenotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвфилесталиксцептион](./esentslvfilestaleexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвфилеункновнексцептион](./esentslvfileunknownexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвхеадербадчекксумексцептион](./esentslvheaderbadchecksumexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвхеадеркорруптедексцептион](./esentslvheadercorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвинвалидпасексцептион](./esentslvinvalidpathexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвовнермапалреадексистсексцептион](./esentslvownermapalreadyexistsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвовнермапкорруптедексцептион](./esentslvownermapcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвовнермаппаженотфаундексцептион](./esentslvownermappagenotfoundexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвпажесноткоммиттедексцептион](./esentslvpagesnotcommittedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвпажеснотделетедексцептион](./esentslvpagesnotdeletedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвпажеснотфриексцептион](./esentslvpagesnotfreeexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвпажеснотресерведексцептион](./esentslvpagesnotreservedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвпровидернотлоадедексцептион](./esentslvprovidernotloadedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвпровидерверсионмисматчексцептион](./esentslvproviderversionmismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвреадверифифаилуриксцептион](./esentslvreadverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. ЕсентслврутнотспеЦифиедексцептион](./esentslvrootnotspecifiedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслврутпасинвалидексцептион](./esentslvrootpathinvalidexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслврутстиллопенексцептион](./esentslvrootstillopenexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвспацекорруптедексцептион](./esentslvspacecorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвспацевритеконфликтексцептион](./esentslvspacewriteconflictexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвстреамингфилеалреадексистсексцептион](./esentslvstreamingfilealreadyexistsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвстреамингфилефуллексцептион](./esentslvstreamingfilefullexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвстреамингфилеинусиксцептион](./esentslvstreamingfileinuseexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвстреамингфилемиссинжексцептион](./esentslvstreamingfilemissingexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвстреамингфиленоткреатедексцептион](./esentslvstreamingfilenotcreatedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентслвстреамингфилереадонлексцептион](./esentslvstreamingfilereadonlyexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентсофтрековерйонснапшотексцептион](./esentsoftrecoveryonsnapshotexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентспаваилексткачеаутофмеморексцептион](./esentspavailextcacheoutofmemoryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентспаваилексткачеаутофсинцексцептион](./esentspavailextcacheoutofsyncexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентскллинкнотсуппортедексцептион](./esentsqllinknotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентстреамингдатанотлогжедексцептион](./esentstreamingdatanotloggedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенттагжеднотнуллексцептион](./esenttaggednotnullexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенттемпфилеопенеррорексцептион](./esenttempfileopenerrorexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенттуманйопендатабасесексцептион](./esenttoomanyopendatabasesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенттуманисплитсексцептион](./esenttoomanysplitsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентуникодетранслатионбуффертусмаллексцептион](./esentunicodetranslationbuffertoosmallexception-class.md)