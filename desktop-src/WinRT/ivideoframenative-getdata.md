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
ms.openlocfilehash: 832b2e300887699b926362ce9cbfc6f334c181805bacb3546532920c684251d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993774"
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

 

 



