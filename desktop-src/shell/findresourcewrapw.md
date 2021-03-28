---
description: Определяет расположение ресурса с указанным типом и именем в указанном модуле.
ms.assetid: d8322430-5064-407e-8b89-b86b75bf139e
title: Функция Финдресаурцеврапв
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindResourceWrapW
- FindResourceWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 8f76d516570725fe6da5e8a21ec5a29699276ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264437"
---
# <a name="findresourcewrapw-function"></a>Функция Финдресаурцеврапв

\[**Финдресаурцеврапв** доступен для использования в Windows XP. Она может быть недоступна в последующих версиях. Вместо этого следует использовать [**финдресаурцев**](/windows/win32/api/winbase/nf-winbase-findresourcea) .\]

Определяет расположение ресурса с указанным типом и именем в указанном модуле.

> [!Note]  
> **Финдресаурцеврапв** — это оболочка для функции **финдресаурцев** . Дополнительные замечания об использовании см. в разделе [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) .

 

## <a name="syntax"></a>Синтаксис


```C++
HRSRC FindResourceWrapW(
  _In_ HMODULE hModule,
  _In_ LPCWSTR lpName,
  _In_ LPCWSTR lpType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хмодуле* \[ окне\]
</dt> <dd>

Тип: **хмодуле**

Обработчик для модуля, исполняемый файл которого содержит ресурс. Значение **null** указывает маркер модуля, связанный с файлом образа, который используется операционной системой для создания текущего процесса.

</dd> <dt>

*лпнаме* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Имя ресурса. Дополнительные сведения см. в разделе [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).

</dd> <dt>

*лптипе* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Указатель на строку, указывающую тип ресурса. Дополнительные сведения см. в разделе [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **хрсрк**

Если функция выполнена, возвращаемое значение является маркером для блока сведений указанного ресурса. Чтобы получить маркер для ресурса, передайте этот обработчик функции [**лоадресаурце**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .

Если функция завершается ошибкой, возвращается значение **null**. Чтобы получить расширенные сведения об ошибке, вызовите функцию [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Примечания

Если необходимо указать определенную локализацию, используйте функцию [**финдресаурцеекс**](/windows/win32/api/winbase/nf-winbase-findresourceexa) , а не **финдресаурцеврапв**.

**Финдресаурцеврапв** предоставляет возможность использования строк Юникода в более старых операционных системах. Предпочтительным методом является использование [**финдресаурцев**](/windows/win32/api/winbase/nf-winbase-findresourcea) в сочетании с уровнем Майкрософт для Юникода (мслу).

**Финдресаурцеврапв** должен вызываться напрямую из Shlwapi.dll с использованием порядкового номера 66.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Нет</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (версия 5,0 или более поздняя)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Финдресаурцеврапв** (Юникод)<br/>                                                                    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea)
</dt> </dl>

 

 
