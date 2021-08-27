---
description: Нельзя получить доступ к сеансу установщика из настраиваемого действия, которое не является текущим сеансом установки.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Доступ к базе данных или сеансу из настраиваемого действия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c653d14bc2fdb361469389c4ee053e5d98b65f8c8265516c4e2c3bd4fc4c96d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046064"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a>Доступ к базе данных или сеансу из настраиваемого действия

Нельзя получить доступ к сеансу установщика из настраиваемого действия, которое не является текущим сеансом установки. Пользовательские действия ограничены работой только с активной базой данных сеанса и без других баз данных. следующие установщик Windows [функции базы данных](database-functions.md) не должны вызываться из настраиваемого действия, так как они нуждаются в обработке базы данных, которая не является базой данных текущего сеанса установки.

[**мсидатабасемерже**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

[**мсикреатетрансформсуммаринфо**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

 

[**мсидатабасеапплитрансформ**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)

 

[**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

 

[**мсидатабасикспорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)

 

[**мсидатабасеженератетрансформ**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)

 

[**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)

 

[**мсиенаблеуипревиев**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)

 

[**мсижетдатабасестате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Доступ к текущему сеансу установщика из пользовательского действия](accessing-the-current-installer-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



