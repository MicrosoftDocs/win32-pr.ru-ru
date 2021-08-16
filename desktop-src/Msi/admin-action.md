---
description: Действие администратора — это действие верхнего уровня, используемое для выполнения административных установок.
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: Действие администратора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785bd69a8de7da1df9a812f7e89d589b6e939b3eedd6b3cecb66bf86407636cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145937"
---
# <a name="admin-action"></a>Действие администратора

Действие администратора — это действие верхнего уровня, используемое для выполнения [административных установок](administrative-installation.md).

## <a name="sequence-restrictions"></a>Ограничения последовательности

Ограничения последовательности отсутствуют.

## <a name="actiondata-messages"></a>Сообщения Актиондата

Нет сообщений Актиондата.

## <a name="remarks"></a>Remarks

действие администратора не вызывается из последовательности таблицы действий, установщик Windows выполняет это действие при вызове [**мсиинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) с параметром *сзкоммандлине* , для которого задано значение action = ADMIN, или исполняемый файл командной строки, Msiexec.exe вызывается с параметром командной строки "/a".

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Таблица Админуисекуенце](adminuisequence-table.md)
</dt> <dt>

[Таблица Админексекутесекуенце](adminexecutesequence-table.md)
</dt> </dl>

 

 



