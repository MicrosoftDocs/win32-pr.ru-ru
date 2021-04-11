---
description: Этот метод возвращает интерфейс, предоставляющий доступ к звуковым данным.
ms.assetid: 4FA7CC9D-D379-4C08-8D4F-5301ECCDF372
title: 'Метод Иаудиофраменативе:: GetData'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAudioFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: eb61bce5132c2029b6f53fdd1159ca50984ba936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145133"
---
# <a name="iaudioframenativegetdata-method"></a>Метод Иаудиофраменативе:: GetData

Этот метод возвращает интерфейс, предоставляющий доступ к звуковым данным.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*riid* \[ окне\]
</dt> <dd>

Тип: **рефиид**

IID получаемого интерфейса.

</dd> <dt>

*ППВ* \[ заполняет\]
</dt> <dd>

Тип: **лпвоид \** _

При успешном возврате этого метода содержит указатель интерфейса, запрошенный в параметре _riid *.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает \_ ОК при успешном завершении. Возвращает E \_ Interface, если не удается найти запрошенный интерфейс.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иаудиофраменативе**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative)
</dt> </dl>

 

 



