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
ms.openlocfilehash: 1bf86a3005a2b865b2096eddc5ffa9c0c33f848a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680119"
---
# <a name="rasadminfreebuffer-function"></a>Функция Расадминфрибуффер

\[Эта функция предоставляется только для обеспечения обратной совместимости с Windows NT Server 4,0. Он возвращает \_ вызов ошибки \_ \_ , не реализованный в Windows Server 2003. Приложения должны использовать функцию [**мпрадминбуфферфри**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) .\]

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

## <a name="remarks"></a>Комментарии

Используйте функцию **расадминфрибуффер** , чтобы освободить буферы, выделенные функциями [**расадминпортенум**](rasadminportenum.md) и [**расадминпортжетинфо**](rasadminportgetinfo.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows 2000 Professional<br/>                                                   |
| Поддержка конца сервера<br/> | Windows 2000 Server<br/>                                                         |
| Header<br/>                | <dl> <dt>Рассапи. h</dt> </dl>   |
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

 

