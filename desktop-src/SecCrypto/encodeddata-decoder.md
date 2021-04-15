---
description: Получает объект декодера, если он существует.
ms.assetid: b8a1c7c9-e7ac-4b0e-a342-5b923ab83df3
title: Метод Енкодеддата. декодер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Decoder
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 334895ed683d0c582628b4b623a7343ca561be22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648948"
---
# <a name="encodeddatadecoder-method"></a>Метод Енкодеддата. декодер

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс асненкодеддата**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Метод **декодера** получает объект декодера, если он существует.

## <a name="syntax"></a>Синтаксис


```VB
EncodedData.Decoder()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="remarks"></a>Комментарии

Если закодированные данные не имеют объекта декодера, возвращается **значение NULL** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
