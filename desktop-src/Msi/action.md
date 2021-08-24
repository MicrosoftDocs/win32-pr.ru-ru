---
description: Для свойства ACTION можно задать следующие значения.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: Свойство ACTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b4f17c7bd08b2e366fa23a55ad2b8044ce845ac4df04d0164ba34ad6dff32b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145997"
---
# <a name="action-property"></a>Свойство ACTION

Для свойства **Action** можно задать следующие значения.

## <a name="value"></a>Значение



| Значение                                                                                                                                            | Значение                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <dt>**ВЗНОС**</dt> </dl>       | [Действие установки](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <dt>**РЕКЛАМИРОВАТЬ**</dt> </dl> | [Действие объявления](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <dt>**ГРУППЫ**</dt> </dl>             | [Действие администратора](admin-action.md)<br/>         |



 

Свойство **Action** определяет, какое действие следует выполнить, если для [**Мсидоактион**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) или [**метода DoAction**](session-doaction.md)задано имя действия null. Если для свойства **Action** не определено значение, установщик вызывает [действие Install](install-action.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP. сведения о минимальном Windows пакета обновления, который требуется для установщик Windows версии, см. в [установщик Windows требования к Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства](properties.md)
</dt> </dl>

 

 




