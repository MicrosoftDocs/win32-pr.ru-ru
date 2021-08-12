---
title: Сообщение WM_COPYDATA (Winuser. h)
description: Приложение отправляет \_ сообщение WM COPYDATA для передачи данных в другое приложение.
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- WM_COPYDATA Exchange данных сообщений
topic_type:
- apiref
api_name:
- WM_COPYDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb91b2544bf0ebf0e8767a611b422de9aaaf1d73161e47c7bf27768f4acecb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304490"
---
# <a name="wm_copydata-message"></a>\_Сообщение COPYDATA WM

Приложение отправляет сообщение **WM \_ COPYDATA** для передачи данных в другое приложение.


```C++
#define WM_COPYDATA                     0x004A
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер окна, который передает данные.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**копидатаструкт**](/windows/win32/api/winuser/ns-winuser-copydatastruct) , содержащую передаваемые данные.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если принимающее приложение обрабатывает это сообщение, оно должно возвращать **значение true**; в противном случае возвращается **значение false**.

## <a name="remarks"></a>Remarks

Передаваемые данные не должны содержать указатели или другие ссылки на объекты, недоступные для приложения, получающего данные.

При отправке этого сообщения данные, на которые указывают ссылки, не должны изменяться другим потоком отправляющего процесса.

Принимающее приложение должно учитывать данные, которые доступны только для чтения. Параметр *lParam* действителен только во время обработки сообщения. Принимающее приложение не должно освобождать память, на которую ссылается *lParam*. Если принимающее приложение должно получить доступ к данным после возврата [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , оно должно скопировать данные в локальный буфер.

## <a name="examples"></a>Примеры

Пример см. в разделе [Использование копирования данных](using-data-copy.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылка**
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**копидатаструкт**](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 

