---
title: Константы TS_LF_ (Текстстор. h)
description: '\_ \_ Константы TS LF \ определяют тип блокировки документа.'
ms.assetid: f0bb6ef9-a8fc-4331-9210-6c5ba1721a73
topic_type:
- apiref
api_name:
- TS_LF_SYNC
- TS_LF_READ
- TS_LF_READWRITE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6240511fd95e91a7f22477f631178dfab528f1e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681750"
---
# <a name="ts_lf_-constants"></a>\_ \_ \* Константы TS LF

\_ \_ \* Константы перевода TS указывают тип блокировки документа.



| Константа/значение                                                                                                                                                                                                                    | Описание                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span id="TS_LF_SYNC"></span><span id="ts_lf_sync"></span><dl> <dt>**TS \_ \_Синхронизация LF**</dt> <dt>(0x1)</dt> </dl>                | Документ имеет синхронную блокировку, если этот флаг сочетается с другими флагами.<br/> |
| <span id="TS_LF_READ"></span><span id="ts_lf_read"></span><dl> <dt>**TS \_ \_Чтение LF**</dt> <dt>(0x2)</dt> </dl>                | Документ имеет блокировку только для чтения и не может быть изменена.<br/>                      |
| <span id="TS_LF_READWRITE"></span><span id="ts_lf_readwrite"></span><dl> <dt>**TS \_ LF \_ ReadWrite**</dt> <dt>(0x6)</dt> </dl> | Документ имеет блокировку чтения и записи и может быть изменен.<br/>                        |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Распространяемые компоненты<br/>          | TSF 1,0 в Windows 2000 профессиональная<br/>                                         |
| Header<br/>                   | <dl> <dt>Текстстор. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Текстстор. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Блокировки документов](document-locks.md)
</dt> <dt>

[ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[ITextStoreACPSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[Итекстстореанчор:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[Итекстстореанчорсинк:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> </dl>

 

 





