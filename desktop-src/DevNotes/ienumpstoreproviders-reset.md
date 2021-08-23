---
description: 'Метод Иенумпсторепровидерс:: Reset — сбрасывается до начала последовательности перечисления.'
ms.assetid: 9c5044b5-25a3-4d10-829b-ef4d8b5ac095
title: 'Метод Иенумпсторепровидерс:: Reset (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3a9214ace99021bebe9529cb8395aa217f8a8305d9ed0f42ab06998328d65f08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691304"
---
# <a name="ienumpstoreprovidersreset-method"></a>Метод Иенумпсторепровидерс:: Reset

\[защищенные служба хранилища (Pstore) доступны для использования в Windows Server 2003 и Windows XP. она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Выполняет сброс до начала последовательности перечисления.

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



## <a name="see-also"></a>См. также

<dl> <dt>

[**иенумпсторепровидерс**](ienumpstoreproviders.md)
</dt> </dl>

 

 
