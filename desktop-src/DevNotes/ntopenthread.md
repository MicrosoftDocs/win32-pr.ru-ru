---
description: Открывает обработчик для объекта потока с указанным доступом.
ms.assetid: 85148f27-cfb4-4a33-8bcc-e48d2c2e3c51
title: Функция Нтопенсреад
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenThread
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8c1b64d2e024f3905d171ab5ca90e59df929ffc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648751"
---
# <a name="ntopenthread-function"></a>Функция Нтопенсреад

\[Эта функция может быть изменена или удалена из Windows без предварительного уведомления. Вместо этого используйте функцию [**опенсреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) .\]

Открывает обработчик для объекта потока с указанным доступом.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS NtOpenThread(
  _Out_ PHANDLE            ThreadHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes,
  _In_  PCLIENT_ID         ClientId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Среадхандле* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает обработчик объекта потока.

</dd> <dt>

*Десиредакцесс* \[ окне\]
</dt> <dd>

Тип [**данных \_ маски доступа**](../secauthz/access-mask-format.md) , предоставляющий требуемые типы доступа для объекта потока.

</dd> <dt>

*Обжектаттрибутес* \[ окне\]
</dt> <dd>

Указатель на структуру [ \_ атрибутов объекта](https://msdn.microsoft.com/library/aa491657.aspx) . Элемент **objectname** этой структуры должен иметь значение null.

**Windows Server 2003 и Windows XP:** Элемент **objectname** этой структуры может указывать на имя объекта. Если **objectname** не равен null, параметр *ClientID* должен иметь значение null.

</dd> <dt>

*ClientID* \[ окне\]
</dt> <dd>

Указатель на структуру **\_ идентификатора клиента** , определяющую поток, чей поток должен быть открыт.

**Windows Server 2003 и Windows XP:** Указатель на структуру **\_ идентификатора клиента** , определяющую поток, чей поток должен быть открыт. Этот параметр может принимать значение NULL. Если этот параметр не равен NULL, то элемент **objectname** структуры, на который указывает параметр *обжектаттрибутес* , должен иметь значение null.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает код **NTSTATUS** или ошибки.

Формы и значения кодов ошибок **NTSTATUS** перечислены в файле заголовка NTSTATUS. h, доступном в WDK, и описаны в документации по WDK.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанного файла заголовка. Связанная библиотека импорта, NTDLL. lib, доступна в WDK. Можно также использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Ntdll.dll.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
