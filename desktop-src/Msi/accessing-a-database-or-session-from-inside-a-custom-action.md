---
description: Нельзя получить доступ к сеансу установщика из настраиваемого действия, которое не является текущим сеансом установки.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Доступ к базе данных или сеансу из настраиваемого действия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839c34fbfcd6cc69c026db455b0c2e3a59a28e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998317"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a>Доступ к базе данных или сеансу из настраиваемого действия

Нельзя получить доступ к сеансу установщика из настраиваемого действия, которое не является текущим сеансом установки. Пользовательские действия ограничены работой только с активной базой данных сеанса и без других баз данных. Следующие установщик Windows [функции базы данных](database-functions.md) не должны вызываться из настраиваемого действия, так как они нуждаются в обработке базы данных, которая не является базой данных текущего сеанса установки.

[**мсидатабасемерже**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

[**мсикреатетрансформсуммаринфо**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

 

[**мсидатабасеапплитрансформ**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)

 

[**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

 

[**мсидатабасикспорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)

 

[**мсидатабасеженератетрансформ**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)

 

[**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)

 

[**мсиенаблеуипревиев**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)

 

[**мсижетдатабасестате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Доступ к текущему сеансу установщика из пользовательского действия](accessing-the-current-installer-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



