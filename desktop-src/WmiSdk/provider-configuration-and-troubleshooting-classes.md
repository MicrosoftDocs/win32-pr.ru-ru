---
description: '\_Класс поставщиков MSFT и классы устранения неполадок WMI представляют собой группу классов событий MSFT, связанных с событиями поставщика WMI.'
ms.assetid: 5eaf7026-87bf-416b-9a6d-7f92f85b0882
ms.tgt_platform: multiple
title: Классы для настройки и устранения неполадок поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be63fb5693898541bffae2abcb05b7595ae7fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712107"
---
# <a name="provider-configuration-and-troubleshooting-classes"></a>Классы для настройки и устранения неполадок поставщика

Класс [**\_ поставщиков MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) и классы устранения неполадок WMI представляют собой группу [классов событий MSFT](msft-classes.md) , связанных с событиями поставщика WMI.

Класс [**\_ поставщиков MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) содержит сведения о конфигурации для поставщиков и включает следующие методы, позволяющие загружать и выгружать поставщиков, а также останавливать и возобновлять операции поставщика.

-   [**Метод Load \_ класса поставщиков MSFT**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers)
-   [**Метод Unload \_ класса поставщиков MSFT**](/previous-versions/windows/desktop/wmisystemprov/unload-method-in-class-msft-providers)
-   [**Метод Resume \_ класса поставщиков MSFT**](/previous-versions/windows/desktop/wmisystemprov/resume-method-in-class-msft-providers)
-   [**Метод Suspend \_ класса поставщиков MSFT**](/previous-versions/windows/desktop/wmisystemprov/suspend-method-in-class-msft-providers)

[Классы устранения неполадок WMI](wmi-troubleshooting-classes.md) называются, чтобы указать, срабатывает ли событие до или после события поставщика. Например, [**\_ \_ \_ Предварительный объект MSFT события AccessCheck**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) создается непосредственно перед вызовом реализации поставщика **ивбемевентсекурити:: AccessCheck**, а объект [**MSFT \_ события \_ AccessCheck \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) вызывается сразу после.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Устранение неполадок WMI](wmi-troubleshooting.md).
</dt> <dt>

[Классы устранения неполадок WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
