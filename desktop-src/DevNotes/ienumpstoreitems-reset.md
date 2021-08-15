---
description: Выполняет сброс до начала данной последовательности перечисления.
ms.assetid: add91f5d-3f84-4069-93c0-9380a3935b85
title: 'Метод Иенумпстореитемс:: Reset (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: ee49de07e59ecd0a16efab1e3cae0d9e52ffe5805857838508ea1ec39e999b7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404577"
---
# <a name="ienumpstoreitemsreset-method"></a>Метод Иенумпстореитемс:: Reset

\[защищенные служба хранилища (Pstore) доступны для использования в Windows Server 2003 и Windows XP. она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Выполняет сброс до начала данной последовательности перечисления.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Reset();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является значением **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иенумпстореитемс**](ienumpstoreitems.md)
</dt> </dl>

 

 
