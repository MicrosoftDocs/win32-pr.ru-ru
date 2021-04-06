---
description: Записывает двоичные данные из указанного файла в указанную базу данных.
ms.assetid: 960633a8-5cec-462b-b7dc-72eb3e4fd0a2
title: Функция Сдбвритебинаритагфромфиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTagFromFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75b45a935fd9630afcefe8f7d30338a6ad6b10a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990467"
---
# <a name="sdbwritebinarytagfromfile-function"></a>Функция Сдбвритебинаритагфромфиле

Записывает двоичные данные из указанного файла в указанную базу данных.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbWriteBinaryTagFromFile(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszPath
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pdb* \[ -файл окне\]
</dt> <dd>

Маркер базы данных оболочек совместимости.

</dd> <dt>

*ттаг* \[ окне\]
</dt> <dd>

ТЕГ для записи. Этот тег должен иметь тип **\_ \_ binary типа Tag**.

</dd> <dt>

*пвсзпас* \[ окне\]
</dt> <dd>

Путь к файлу, содержащему данные. Этот параметр не может иметь **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбвритебинаритаг**](sdbwritebinarytag.md)
</dt> </dl>

 

 




