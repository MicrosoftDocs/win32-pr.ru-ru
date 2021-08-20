---
title: Перечисление Вмундоактион (Впккоминтерфацес. h)
description: Указывает, что произойдет для отмены дисков при выключении или отключении виртуальной машины.
ms.assetid: f8f96fd3-0b2a-40ae-8b2e-b6bcc995dedd
keywords:
- Перечисление Вмундоактион Virtual PC
topic_type:
- apiref
api_name:
- VMUndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f62c4ab00b30300b2951a5a6b1c300bf34b1b3797f036f28a66e82dc2cad22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998334"
---
# <a name="vmundoaction-enumeration"></a>Перечисление Вмундоактион

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Указывает, что произойдет для отмены дисков при выключении или отключении виртуальной машины.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  vmUndoAction_Discard  = 0,
  vmUndoAction_Keep     = 1,
  vmUndoAction_Commit   = 2
} VMUndoAction;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**Вмундоактион \_ отбросить**
</dt> <dd>

Отменить диски отмены; родительские диски остаются без изменений.

</dd> <dt>

<span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**Вмундоактион \_**
</dt> <dd>

Не отключайте диски отмены. родительские диски остаются без изменений, но изменения будут поддерживаться при следующем запуске виртуальной машины.

</dd> <dt>

<span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**Вмундоактион \_ фиксация**
</dt> <dd>

Зафиксируйте изменения на родительских дисках.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Ивмвиртуалмачине:: Ундоактион**](ivmvirtualmachine-undoaction.md)
</dt> </dl>

 

