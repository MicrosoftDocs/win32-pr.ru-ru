---
description: Отправляется в библиотеку DLL расширения, когда диспетчер файлов загружает библиотеку DLL.
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: Сообщение FMEVENT_LOAD (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 8001ca861b77755ea7f5ee829a9af490c2f426dcd6179f2fe84831c624bb4ef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860659"
---
# <a name="fmevent_load-message"></a>\_Сообщение о загрузке фмевент

Отправляется в библиотеку DLL расширения, когда диспетчер файлов загружает библиотеку DLL.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*лпфмслд* 
</dt> <dd>

Адрес структуры [**\_ загрузки FMS**](fms-load.md) , указывающей разностное значение пункта меню.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Библиотека DLL расширения должна возвращать **значение true** , чтобы продолжить загрузку библиотеки DLL. Если библиотека DLL возвращает **значение false**, диспетчер файлов вызывает функцию [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) и завершает все взаимодействие с библиотекой DLL расширения.

## <a name="remarks"></a>Remarks

Приложение должно заполнить элементы **двсизе**, **сзменунаме** и **HMENU** в структуре [**\_ загрузки FMS**](fms-load.md) . Он также должен сохранить значение элемента **вменуделта** и использовать его для обнаружения пунктов меню при изменении меню.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Вфекст. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**фмекстенсионпрок**](fmextensionproc.md)
</dt> </dl>

 

 
