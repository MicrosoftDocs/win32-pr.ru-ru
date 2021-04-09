---
title: Функция Сисфриаллокатедмемори (Сисбкуп. h)
description: Освобождает память, выделенную функциями API SIS.
ms.assetid: 8fab79c8-593c-46df-a885-09a59620a977
keywords:
- Резервное копирование функции Сисфриаллокатедмемори
topic_type:
- apiref
api_name:
- SisFreeAllocatedMemory
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724970817b89f6a9f2490b0776775f6a3a4e69ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891657"
---
# <a name="sisfreeallocatedmemory-function"></a>Функция Сисфриаллокатедмемори

Функция **сисфриаллокатедмемори** освобождает память, выделенную ФУНКЦИЯМИ API SIS.

## <a name="syntax"></a>Синтаксис


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*аллокатедспаце* \[ окне\]
</dt> <dd>

Указатель на память, выделенную API SIS.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

После завершения вызова этой функции вызывающий может больше не обращаться к освобожденной памяти.

Этот вызов следует использовать для освобождения памяти, выделенной для строк параметров *коммонсторерутпаснаме* , возвращаемых из [**сискреатебаккупструктуре**](siscreatebackupstructure.md) и [**сискреатерестореструктуре**](siscreaterestorestructure.md), и массива строк, содержащих имена файлов общего хранилища, возвращаемые из **сискреатебаккупструктуре**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure** и [**SisRestoredLink**](sisrestoredlink.md). В последнем случае массив также должен быть освобожден путем вызова **сисфриаллокатедмемори**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Сисбкуп. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Сисбкуп. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сискреатебаккупструктуре**](siscreatebackupstructure.md)
</dt> <dt>

[**сискреатерестореструктуре**](siscreaterestorestructure.md)
</dt> <dt>

[**сисксфилестобаккупфорлинк**](siscsfilestobackupforlink.md)
</dt> <dt>

[**сисресторедлинк**](sisrestoredlink.md)
</dt> </dl>

 

 





