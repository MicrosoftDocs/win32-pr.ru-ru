---
description: Выполняет поиск указанного исполняемого файла.
ms.assetid: 32c6b054-7e47-4427-bdfe-6b5066db4ac3
title: Функция Сдбжетматчинжексе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9f359db3d34b05455ae75b681a9051ebed927c06c3802b8d2c366fa552594666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390204"
---
# <a name="sdbgetmatchingexe-function"></a>Функция Сдбжетматчинжексе

Выполняет поиск указанного исполняемого файла.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbGetMatchingExe(
  _In_opt_ HSDB            hSDB,
  _In_     LPCTSTR         szPath,
  _In_opt_ LPCTSTR         szModuleName,
  _In_opt_ LPCTSTR         pszEnvironment,
  _In_     DWORD           dwFlags,
  _Out_    PSDBQUERYRESULT pQueryResult
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хсдб* \[ в необязательное\]
</dt> <dd>

Маркер базы данных оболочек совместимости, возвращаемый функцией [**сдбинитдатабасе**](sdbinitdatabase.md) .

</dd> <dt>

*сзпас* \[ окне\]
</dt> <dd>

Путь к исполняемому файлу.

</dd> <dt>

*сзмодуленаме* \[ в необязательное\]
</dt> <dd>

Имя модуля.

</dd> <dt>

*псзенвиронмент* \[ в необязательное\]
</dt> <dd>

Переменные среды, используемые в качестве контекста поиска.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Этот параметр может иметь значение 0 или **сдбгмеф \_ игнорировать \_ окружение** (0x1).

</dd> <dt>

*пкуериресулт* \[ заполняет\]
</dt> <dd>

Структура [**сдбкуериресулт**](sdbqueryresult.md) . Если совпадений не найдено, структура содержит **тагреф \_ null**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="remarks"></a>Remarks

Завершив работу с возвращенным [**тагреф**](tagref.md), освободите его с помощью функции [**сдбрелеасематчинжексе**](sdbreleasematchingexe.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбинитдатабасе**](sdbinitdatabase.md)
</dt> <dt>

[**сдбрелеасематчинжексе**](sdbreleasematchingexe.md)
</dt> </dl>

 

 




