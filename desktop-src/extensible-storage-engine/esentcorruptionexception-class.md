---
description: 'Дополнительные сведения о: Есенткорруптионексцептион Class'
title: Класс EsentCorruptionException
TOCTitle: EsentCorruptionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCorruptionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a6914c2bf133a1050e3e3800e5c113c6cac1a11f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104273203"
---
# <a name="esentcorruptionexception-class"></a>Класс EsentCorruptionException

Базовый класс для исключений повреждения.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион  
            

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentCorruptionException _
    Inherits EsentDataException
'Usage
Dim instance As EsentCorruptionException
```

``` csharp
[SerializableAttribute]
public abstract class EsentCorruptionException : EsentDataException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Элементы Есенткорруптионексцептион](./esentcorruptionexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Производные типы

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион  
            [Microsoft. ISAM. ESENT. Interop. Есентбадемптипажеексцептион](./esentbademptypageexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентбадпажелинкексцептион](./esentbadpagelinkexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентбадпарентпажелинкексцептион](./esentbadparentpagelinkexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенткаталогкорруптедексцептион](./esentcatalogcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентчеккпоинткорруптексцептион](./esentcheckpointcorruptexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенткоммиттедлогфилекорруптексцептион](./esentcommittedlogfilecorruptexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенткоммиттедлогфилесмиссинжексцептион](./esentcommittedlogfilesmissingexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. ЕсентдатабасебуффердепенденЦиескорруптедексцептион](./esentdatabasebufferdependenciescorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдатабасекорруптедексцептион](./esentdatabasecorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдбтимекорруптедексцептион](./esentdbtimecorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдекомпрессионфаиледексцептион](./esentdecompressionfailedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдериведколумнкорруптионексцептион](./esentderivedcolumncorruptionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентдискреадверификатионфаилуриксцептион](./esentdiskreadverificationfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентфилеиобэйондеофексцептион](./esentfileiobeyondeofexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентфилесистемкорруптионексцептион](./esentfilesystemcorruptionexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентиндексбуилдкорруптедексцептион](./esentindexbuildcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентинвалидлогсекуенцеексцептион](./esentinvalidlogsequenceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлогкорруптдурингхардрековерексцептион](./esentlogcorruptduringhardrecoveryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлогкорруптдурингхардресториксцептион](./esentlogcorruptduringhardrestoreexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлогкорруптедексцептион](./esentlogcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлогфилекорруптексцептион](./esentlogfilecorruptexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлогреадверифифаилуриксцептион](./esentlogreadverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлогторнвритедурингхардрековерексцептион](./esentlogtornwriteduringhardrecoveryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлогторнвритедурингхардресториксцептион](./esentlogtornwriteduringhardrestoreexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлвкорруптедексцептион](./esentlvcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентмиссинглогфиликсцептион](./esentmissinglogfileexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентмиссингпревиауслогфиликсцептион](./esentmissingpreviouslogfileexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентпаженотинитиализедексцептион](./esentpagenotinitializedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентпримариндекскорруптедексцептион](./esentprimaryindexcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентреадлостфлушверифифаилуриксцептион](./esentreadlostflushverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентреадпгноверифифаилуриксцептион](./esentreadpgnoverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентреадверифифаилуриксцептион](./esentreadverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентрекордформатконверсионфаиледексцептион](./esentrecordformatconversionfailedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентрековериверифифаилуриксцептион](./esentrecoveryverifyfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентредоабруптендедексцептион](./esentredoabruptendedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентсекондариндекскорруптедексцептион](./esentsecondaryindexcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентспаваилексткорруптедексцептион](./esentspavailextcorruptedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентсповнексткорруптедексцептион](./esentspownextcorruptedexception-class.md)