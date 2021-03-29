---
description: Приложения могут создавать файлы минидампа пользовательского режима, которые содержат полезное подмножество данных, содержащихся в файле аварийного дампа.
ms.assetid: c5de86a4-6dab-4408-8093-66117eb4de10
title: Файлы минидампа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fcd57611cd0b6e5f4f5abdf8bc535f8222feb7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141026"
---
# <a name="minidump-files"></a>Файлы минидампа

Приложения могут создавать файлы минидампа пользовательского режима, которые содержат полезное подмножество данных, содержащихся в файле аварийного дампа. Приложения могут быстро и эффективно создавать файлы минидампа. Так как файлы минидампа невелики, их можно легко отправить через Интернет в службу технической поддержки для приложения.

Файл минидампа не содержит столько сведений, сколько полный файл дампа, но содержит достаточно сведений для выполнения основных операций отладки. Для чтения файла минидампа необходимы двоичные файлы и файл символов, доступные для отладчика.

Текущие версии Microsoft Office и Microsoft Windows создают файлы минидампа с целью анализа сбоев на компьютерах клиентов.

Для файлов минидампа используются следующие функции DbgHelp.

<dl>

[**минидумпкаллбакк**](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[**минидумпреаддумпстреам**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[**минидумпвритедумп**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



