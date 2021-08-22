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
ms.openlocfilehash: a4510e464c2201952823d144721614caa7b5f1397c68f4f129dac73a4015b86a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702184"
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

## <a name="remarks"></a>Remarks

После завершения вызова этой функции вызывающий может больше не обращаться к освобожденной памяти.

Этот вызов следует использовать для освобождения памяти, выделенной для строк параметров *коммонсторерутпаснаме* , возвращаемых из [**сискреатебаккупструктуре**](siscreatebackupstructure.md) и [**сискреатерестореструктуре**](siscreaterestorestructure.md), и массива строк, содержащих имена файлов общего хранилища, возвращаемые из **сискреатебаккупструктуре**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure** и [**SisRestoredLink**](sisrestoredlink.md). В последнем случае массив также должен быть освобожден путем вызова **сисфриаллокатедмемори**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| Заголовок<br/>                   | <dl> <dt>Сисбкуп. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Сисбкуп. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сискреатебаккупструктуре**](siscreatebackupstructure.md)
</dt> <dt>

[**сискреатерестореструктуре**](siscreaterestorestructure.md)
</dt> <dt>

[**сисксфилестобаккупфорлинк**](siscsfilestobackupforlink.md)
</dt> <dt>

[**сисресторедлинк**](sisrestoredlink.md)
</dt> </dl>

 

 





