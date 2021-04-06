---
description: Действие администратора — это действие верхнего уровня, используемое для выполнения административных установок.
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: Действие администратора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00106c9ab7877918e122f1ec9bd201fe30bb68b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909127"
---
# <a name="admin-action"></a>Действие администратора

Действие администратора — это действие верхнего уровня, используемое для выполнения [административных установок](administrative-installation.md).

## <a name="sequence-restrictions"></a>Ограничения последовательности

Ограничения последовательности отсутствуют.

## <a name="actiondata-messages"></a>Сообщения Актиондата

Нет сообщений Актиондата.

## <a name="remarks"></a>Комментарии

Действие администратора не вызывается из последовательности таблицы действий, установщик Windows выполняет это действие при вызове [**мсиинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) с параметром *сзкоммандлине* , для которого задано значение Action = Admin, или исполняемый файл командной строки, Msiexec.exe вызывается с параметром командной строки "/a".

## <a name="related-topics"></a>См. также

<dl> <dt>

[Таблица Админуисекуенце](adminuisequence-table.md)
</dt> <dt>

[Таблица Админексекутесекуенце](adminexecutesequence-table.md)
</dt> </dl>

 

 



