---
description: Запрашивает состояние чтения/записи для области декодирования видео DirectX Acceleration (ДКСВА).
ms.assetid: 8a4c3173-5911-49ec-8cb8-e30f96a4f1c9
title: 'Метод IDirect3DDXVADevice9:: QueryStatus (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.QueryStatus
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: ae2b16ef27b1e172b7927652304104563e120709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711347"
---
# <a name="idirect3ddxvadevice9querystatus-method"></a>Метод IDirect3DDXVADevice9:: QueryStatus

Запрашивает состояние чтения/записи для области декодирования видео DirectX Acceleration (ДКСВА).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT QueryStatus(
   IDirect3DSurface9 *pSurface,
   DWORD             Flags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псурфаце* 
</dt> <dd>

Указатель на интерфейс **IDirect3DSurface9** области для запроса.

</dd> <dt>

*Флаги* 
</dt> <dd>

Указывает тип выполняемого запроса.



| Значение                                                                                                                             | Значение                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="0x00"></span><span id="0X00"></span><dl> <dt>**0x00**</dt> </dl> | Проверьте, является ли поверхность надежной для записи.<br/> |
| <span id="0x01"></span><span id="0X01"></span><dl> <dt>**0x01**</dt> </dl> | Проверьте, является ли поверхность надежно используемой для чтения.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                    |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                              |
| Header<br/>                   | <dl> <dt>Дксва. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




