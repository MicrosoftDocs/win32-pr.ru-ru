---
description: Действие установки — это действие верхнего уровня, которое вызывается для установки или удаления компонентов.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: Действие установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5f648084b7386465f6bb59dd6b523cb51489e4cb83677c0b5cb47fe845be42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811004"
---
# <a name="install-action"></a>Действие установки

Действие установки — это действие верхнего уровня, которое вызывается для установки или удаления компонентов. Это действие запрашивает [таблицу инсталлуисекуенце](installuisequence-table.md) и [таблицу инсталлексекутесекуенце](installexecutesequence-table.md) для выполнения действия, условия для выполнения действия и место действия в последовательности:

## <a name="sequence-restrictions"></a>Ограничения последовательности

Ограничения последовательности отсутствуют.

## <a name="actiondata-messages"></a>Сообщения Актиондата

Нет сообщений Актиондата.

## <a name="remarks"></a>Remarks

действие установки не вызывается из последовательности таблицы действий, передается установщик Windows при вызове [**мсиинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) или в исполняемом файле командной строки, Msiexec.exe вызывается с параметром командной строки "**/i**" или при вызове любой функции установщика, которая может выполнять задачу установки, например [**мсиконфигурефеатуре**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**мсипровидекомпонент**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)или [**мсиинсталлмиссингфиле**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).

 

 



