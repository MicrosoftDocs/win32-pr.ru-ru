---
description: Используется с \_ \_ управляющим кодом ioctl SCSI минипорта IOCTL и ктлкоде \_ искситгт \_ СПТ \_ Session \_ End (0x101) для завершения сеанса.
ms.assetid: 74DAA560-A5BA-475C-AA36-7E6F0EA82EFE
title: Структура ISCSITGT_SPT_SESSION_STOP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCSITGT_SPT_SESSION_STOP
api_type:
- NA
api_location: ''
ms.openlocfilehash: e4501fbe2d1bbf884448d6b6a9476ee4782d3da7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "103914291"
---
# <a name="iscsitgt_spt_session_stop-structure"></a>\_Структура искситгт СПТ \_ сеанса \_

\[Следующая структура доступна для использования в Windows Server 2012 R2. В последующих версиях он может быть изменен или недоступен.\]

Используется с управляющим кодом ioctl [**\_ SCSI \_ МИНИПОРТА**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) IOCTL и ктлкоде \_ искситгт \_ СПТ \_ Session \_ End (0x101) для завершения сеанса.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _ISCSITGT_SPT_SESSION_STOP {
  SRB_IO_CONTROL Header;
  SESSION_COOKIE ITNexusHandle;
} ISCSITGT_SPT_SESSION_STOP, *PISCSITGT_SPT_SESSION_STOP;
```



## <a name="members"></a>Члены

<dl> <dt>

**Header**
</dt> <dd>

Обязательный заголовок.

</dd> <dt>

**итнексушандле**
</dt> <dd>

Непрозрачный маркер, представляющий сеанс.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                               |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/> |
| Окончание поддержки клиента<br/>    | Ни одна версия не поддерживается<br/>                               |
| Поддержка конца сервера<br/>    | Windows Server 2012 R2<br/>                       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Передача цели iSCSI](/powershell/module/iscsi)
</dt> <dt>

[**\_элемент управления вводом-выводом СРБ \_**](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_srb_io_control)
</dt> </dl>

 

 
