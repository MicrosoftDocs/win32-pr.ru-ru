---
description: Список защищенных файлов.
ms.assetid: 46a1ff83-afed-4ce3-bb62-551446efdb78
title: Функция Сфкжетфилес (Сфкфилес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SfcGetFiles
api_type:
- DllExport
api_location:
- Sfcfiles.dll
ms.openlocfilehash: 3201621808708229419542acd7fa0caab0aa7f6e7d38bfe723b7f53bc68c4005
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999284"
---
# <a name="sfcgetfiles-function"></a>Функция Сфкжетфилес

\[Эта функция доступна для использования в операционных системах, указанных в разделе требования. поддержка этой функции была удалена в Windows Vista и Windows Server 2008. Вместо этого используйте поддерживаемые функции, перечисленные в [функциях WRP](wfp-functions.md) .\]

Список защищенных файлов.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI SfcGetFiles(
  _Out_ PPROTECT_FILE_ENTRY ProtFileData,
  _Out_ PULONG              FileCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Протфиледата* \[ заполняет\]
</dt> <dd>

Указатель на структуру [**\_ \_ записи файла ппротект**](pprotect-file-entry.md) , содержащую список защищенных файлов.

</dd> <dt>

*Filecount* \[ заполняет\]
</dt> <dd>

Указатель на расположение, содержащее значение ULONG, которое является числом защищенных файлов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается значение STATUS \_ Success. Если функция завершается с ошибкой, возвращается соответствующий код ошибки NTSTATUS.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                   |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Сфкфилес. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Sfcfiles.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_запись файла \_ ппротект**](pprotect-file-entry.md)
</dt> </dl>

 

 




