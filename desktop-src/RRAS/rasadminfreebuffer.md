---
title: Функция Расадминфрибуффер (Рассапи. h)
description: Функция Расадминфрибуффер освобождает память, выделенную службой RAS от имени вызывающего объекта.
ms.assetid: 6dfbba22-3af1-4771-8c22-506996f30c6b
keywords:
- RAS функции Расадминфрибуффер
topic_type:
- apiref
api_name:
- RasAdminFreeBuffer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9550c072840fabf5d862e32f3bbdc6c26d3b32faf9cf6bf6dcfeae1be400e0a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789099"
---
# <a name="rasadminfreebuffer-function"></a>Функция Расадминфрибуффер

\[эта функция предоставляется только для обеспечения обратной совместимости с Windows NT Server 4,0. он возвращает \_ вызов ошибки \_ \_ , не реализованный на сервере Windows 2003. Приложения должны использовать функцию [**мпрадминбуфферфри**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) .\]

Функция **расадминфрибуффер** освобождает память, ВЫДЕЛЕННУЮ службой RAS от имени вызывающего объекта.

## <a name="syntax"></a>Синтаксис


```C++
DWORD RasAdminFreeBuffer(
  _In_ PVOID Pointer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Указатель мыши* \[ окне\]
</dt> <dd>

Указатель на буфер для освобождения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается значение ошибки \_ Success.

Если функция завершается ошибкой, возвращаемое значение может быть следующим кодом ошибки.



| Значение                                                                                                    | Значение                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**Ошибка \_ недопустимого \_ параметра**</dt> </dl> | Недопустимый параметр *указателя* .<br/> |



 

Расширенные сведения об ошибке для этой функции отсутствуют. не вызывайте [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarks

Используйте функцию **расадминфрибуффер** , чтобы освободить буферы, выделенные функциями [**расадминпортенум**](rasadminportenum.md) и [**расадминпортжетинфо**](rasadminportgetinfo.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows 2000 Professional<br/>                                                   |
| Поддержка конца сервера<br/> | Windows 2000 Server<br/>                                                         |
| Заголовок<br/>                | <dl> <dt>Рассапи. h</dt> </dl>   |
| Библиотека<br/>               | <dl> <dt>Рассапи. lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Обзор службы удаленного доступа (RAS)](about-remote-access-service.md)
</dt> <dt>

[Функции администрирования сервера RAS](ras-server-administration-functions.md)
</dt> <dt>

[**расадминпортенум**](rasadminportenum.md)
</dt> <dt>

[**расадминпортжетинфо**](rasadminportgetinfo.md)
</dt> </dl>

 

