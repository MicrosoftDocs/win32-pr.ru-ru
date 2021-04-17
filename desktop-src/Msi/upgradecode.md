---
description: Свойство UpgradeCode представляет собой идентификатор GUID, представляющий связанный набор продуктов. Значение UpgradeCode используется в таблице Upgrade для поиска связанных версий уже установленных продуктов. Это свойство используется действием Регистерпродукт.
ms.assetid: 6cdee5d8-8aa0-4fad-9338-152ee33b8077
title: UpgradeCode, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e5493ad651e609f6ef9d7ae14e07c0c15b5b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651903"
---
# <a name="upgradecode-property"></a>UpgradeCode, свойство

Свойство **UpgradeCode** представляет собой идентификатор GUID, представляющий связанный набор продуктов. Значение **UpgradeCode** используется в [таблице Upgrade](upgrade-table.md) для поиска связанных версий уже установленных продуктов.

Это свойство используется [действием регистерпродукт](registerproduct-action.md).

## <a name="remarks"></a>Комментарии

Настоятельно рекомендуется, чтобы авторы установочных пакетов указали **UpgradeCode** для своего приложения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Установщик Windows в Windows Server 2003 или Windows XP. Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства](properties.md)
</dt> <dt>

[Установка исправлений и обновления](patching-and-upgrades.md)
</dt> <dt>

[Подготовка приложения к будущим основным обновлениям](preparing-an-application-for-future-major-upgrades.md)
</dt> </dl>

 

 




