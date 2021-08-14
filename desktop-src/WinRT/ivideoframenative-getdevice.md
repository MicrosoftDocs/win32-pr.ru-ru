---
description: Этот метод возвращает устройство, связанное с данными видео.
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
title: 'Метод Ивидеофраменативе:: of Device'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetDevice
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: 7f204cc0d44690a2b80c8642d590ef38510cebedbc00332720ec51529fe34ad2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323113"
---
# <a name="ivideoframenativegetdevice-method"></a>Метод Ивидеофраменативе:: of Device

Этот метод возвращает устройство, связанное с данными видео.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDevice(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*riid* \[ окне\]
</dt> <dd>

Идентификатор IID извлекаемого устройства.

</dd> <dt>

*ППВ* \[ заполняет\]
</dt> <dd>

При успешном возврате этого метода содержит указатель устройства, запрошенный в параметре *riid* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ ОК при успешном завершении.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивидеофраменативе**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



