---
description: Отправляется расширением диспетчера файлов (или другим приложением), чтобы диспетчер файлов перезагружал все библиотеки DLL расширения, перечисленные в \[ разделе "надстройки" \] файла Winfile.ini.
ms.assetid: 5103a986-5f45-4deb-aaae-c6e87cb60051
title: Сообщение FM_RELOAD_EXTENSIONS (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_RELOAD_EXTENSIONS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 9e4e632ac153a78e729ce0d3fcd65f49ae90781bd29cfe354d4571ba04e63be0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224178"
---
# <a name="fm_reload_extensions-message"></a>\_Сообщение о перезагрузке \_ расширений FM

Отправляется расширением диспетчера файлов (или другим приложением), чтобы диспетчер файлов перезагружал все библиотеки DLL расширения, перечисленные в \[ разделе "надстройки" \] файла Winfile.ini.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Другие приложения могут использовать функцию посылки [**сообщений**](/windows/win32/api/winuser/nf-winuser-postmessagea) для отправки этого сообщения в Диспетчер файлов. Чтобы получить соответствующий обработчик окна диспетчера файлов, приложение может указать "ВФС \_ Frame" в качестве параметра *лпсзкласснаме* в вызове функции [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) .

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

 

 
