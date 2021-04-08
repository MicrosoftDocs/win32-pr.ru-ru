---
description: Действие установки — это действие верхнего уровня, которое вызывается для установки или удаления компонентов.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: Действие установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04279ba66f189ff83146fc2010e6843c20b404d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080624"
---
# <a name="install-action"></a>Действие установки

Действие установки — это действие верхнего уровня, которое вызывается для установки или удаления компонентов. Это действие запрашивает [таблицу инсталлуисекуенце](installuisequence-table.md) и [таблицу инсталлексекутесекуенце](installexecutesequence-table.md) для выполнения действия, условия для выполнения действия и место действия в последовательности:

## <a name="sequence-restrictions"></a>Ограничения последовательности

Ограничения последовательности отсутствуют.

## <a name="actiondata-messages"></a>Сообщения Актиондата

Нет сообщений Актиондата.

## <a name="remarks"></a>Комментарии

Действие установки не вызывается из последовательности таблицы действий, передается установщик Windows при вызове [**мсиинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) или в исполняемом файле командной строки, Msiexec.exe вызывается с параметром командной строки "**/i**" или при вызове любой функции установщика, которая может выполнять задачу установки, например [**мсиконфигурефеатуре**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**мсипровидекомпонент**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)или [**мсиинсталлмиссингфиле**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).

 

 



