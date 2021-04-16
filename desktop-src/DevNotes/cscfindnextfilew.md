---
description: Возобновляет операцию поиска файлов.
ms.assetid: 5b1a8f67-7fce-4ba5-918d-826bdaca1947
title: Функция Кскфинднекстфилев
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindNextFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 50b387a1ff99a95fcbe0fae8fe8ad93d14c335b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657425"
---
# <a name="cscfindnextfilew-function"></a>Функция Кскфинднекстфилев

\[Эта функция не поддерживается и не должна использоваться.\]

Возобновляет операцию поиска файлов.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CSCFindNextFileW(
  _In_  HANDLE           hFind,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _In_  FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хфинд* \[ окне\]
</dt> <dd>

Маркер поиска, возвращаемый функцией [**кскфиндфирстфилев**](cscfindfirstfilew.md) .

</dd> <dt>

*lpFind32* \[ заполняет\]
</dt> <dd>

Указатель на структуру [**данных Win32 \_ Find \_**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) , которая получает сведения о файле или подкаталоге.

</dd> <dt>

*лпдвстатус* \[ заполняет\]
</dt> <dd>

Код NTSTATUS, указывающий состояние вызова.

</dd> <dt>

*лпдвпинкаунт* \[ заполняет\]
</dt> <dd>

Этот параметр имеет ненулевое значение, если файл был сделан доступным в автономном режиме или 0 в противном случае.

</dd> <dt>

*лпдвхинтфлагс* \[ заполняет\]
</dt> <dd>

Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                                                                                                                | Значение                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <dt>**Флаг \_ \_Код CSC \_ Указание \_ пользователя**</dt> <dt>0x01</dt> </dl>                                | Пользователь сделал файл доступным в автономном режиме.<br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <dt>**Флаг \_ \_ \_ ПИН-код подсказки CSC \_ наследует \_ пользователя**</dt> <dt>0x02</dt> </dl>       | Пользователь сделал родительский доступ к автономной версии и отметил родительский элемент таким образом, чтобы его дочерние элементы были доступны в автономном режиме.<br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <dt>**Флаг \_ \_ \_ ПИН-код ПОДсказок CSC \_ наследует \_ системные**</dt> <dt>0x04</dt> </dl> | Администратор или групповая политика выполнила доступ к родительскому объекту в автономном режиме и отметил родительский элемент таким образом, что его дочерние элементы доступны в автономном режиме<br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <dt>**Флаг \_ Подсказка CSC для \_ \_ \_ системы закрепления**</dt> <dt>0x10</dt> </dl>                          | Администратор или групповая политика выполнила автономный доступ к файлу.<br/>                                                                      |



 

</dd> <dt>

*лпоргфилетиме* \[ окне\]
</dt> <dd>

Указатель на структуру [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) для получения сведений о дате и времени для файла или подкаталога.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
