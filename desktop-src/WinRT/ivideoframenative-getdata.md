---
description: Этот метод возвращает интерфейс, предоставляющий доступ к данным видео.
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
title: 'Метод Ивидеофраменативе:: GetData'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: c612d2d34e23b393921f83f7dbe9e189aa366b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991120"
---
# <a name="ivideoframenativegetdata-method"></a>Метод Ивидеофраменативе:: GetData

Этот метод возвращает интерфейс, предоставляющий доступ к данным видео.

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

IID получаемого интерфейса.

</dd> <dt>

*ППВ* \[ заполняет\]
</dt> <dd>

При успешном возврате этого метода содержит указатель интерфейса, запрошенный в параметре *riid* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ ОК при успешном завершении. Возвращает E \_ Interface, если не удается найти запрошенный интерфейс.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивидеофраменативе**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



