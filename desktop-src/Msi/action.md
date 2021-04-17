---
description: Для свойства ACTION можно задать следующие значения.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: Свойство ACTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901061f953ffaed030ff6d3a94f440eada25fc59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652034"
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
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Установщик Windows в Windows Server 2003 или Windows XP. Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства](properties.md)
</dt> </dl>

 

 




