---
description: Возвращает список сохраненных файлов конфигурации резервных копий, которые можно восстановить.
ms.assetid: 9487c50e-ef3b-425f-92ef-0614290e9af4
ms.tgt_platform: multiple
title: Метод Листбаккупс класса Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ListBackups
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: ba6a3f042a6bd8f01e4bede00e22bda95ca28ebe7cc2beb33a12c6b49deba6bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589124"
---
# <a name="listbackups-method-of-the-control-class"></a>Метод Листбаккупс класса Control

Возвращает список сохраненных файлов конфигурации резервных копий, которые можно восстановить.

## <a name="syntax"></a>Синтаксис


```mof
void ListBackups(
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string Files[],
  [out] Uint32 FilesTimestampLow[],
  [out] Uint32 FilesTimestampHigh[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Оригиналтиместамплов* \[ заполняет\]
</dt> <dd>

Метка времени установки текущей конфигурации (если она восстановлена из резервной копии, будет содержать исходную метку времени). Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Оригиналтиместамфигх* \[ заполняет\]
</dt> <dd>

Метка времени установки текущей конфигурации (если она восстановлена из резервной копии, будет содержать исходную метку времени). Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Файлы* \[ заполняет\]
</dt> <dd>

Список доступных файлов резервных копий в порядке от самых новых к старым.

</dd> <dt>

*Филестиместамплов* \[ заполняет\]
</dt> <dd>

Для каждого файла резервной копии — метка времени, когда была задана ее конфигурация. Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Филестиместамфигх* \[ заполняет\]
</dt> <dd>

Для каждого файла резервной копии — метка времени, когда была задана ее конфигурация. Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                          |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                       |
| Пространство имен<br/>                | корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор<br/>                                              |
| MOF<br/>                      | <dl> <dt>Бутевентколлекторвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Элемент**](control.md)
</dt> </dl>

 

