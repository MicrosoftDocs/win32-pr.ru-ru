---
description: Создает автономный куст реестра, содержащий один пустой корневой ключ.
ms.assetid: 985cfea4-6f15-4d63-8e41-df2a490296a3
title: Функция Оркреатехиве (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 47454169bee21012010fd7deacec6c1faf3a7d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649010"
---
# <a name="orcreatehive-function"></a>Функция Оркреатехиве

Создает автономный куст реестра, содержащий один пустой корневой ключ.

## <a name="syntax"></a>Синтаксис


```C++
DWORD ORCreateHive(
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фкресулт* \[ заполняет\]
</dt> <dd>

Указывает на переменную для получения маркера корневого ключа только что созданного автономного куста реестра. Если не удается создать куст, функция присваивает этому параметру **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается значение ошибки \_ Success.

Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.

Если недостаточно памяти для создания куста реестра, функция возвращает ошибку \_ \_ недостаточно \_ памяти.

## <a name="remarks"></a>Комментарии

Функция **оркреатехиве** создает пустой куст автономного реестра в памяти. Используйте функции [**оркреатекэй**](orcreatekey.md) и [**орсетвалуе**](orsetvalue.md) , чтобы добавить ключи и задать их значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|---------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | Автономная библиотека реестра Windows версии 1,0 или более поздней<br/>                      |
| Header<br/>          | <dl> <dt>Оффрег. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**оркреатекэй**](orcreatekey.md)
</dt> <dt>

[**оропенхиве**](oropenhive.md)
</dt> <dt>

[**орсавехиве**](orsavehive.md)
</dt> <dt>

[**орсетвалуе**](orsetvalue.md)
</dt> </dl>

 

 
