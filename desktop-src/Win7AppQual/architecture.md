---
description: Слабо связанный Internet Explorer (ЛЦИЕ) повышает надежность обозревателя за счет разделения компонентов и ослабления их взаимозависимости.
ms.assetid: 7609090E-7E2B-4B1F-80FF-192B30A40244
title: Архитектура (Windows 7 и Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6edd27246b7b19765288a280bd467de86d2fe50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818465"
---
# <a name="architecture-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Архитектура (Windows 7 и Windows Server 2008 R2 Application Quality Cookbook)

*Слабо связанный Internet Explorer* (лЦие) повышает надежность обозревателя за счет разделения компонентов и ослабления их взаимозависимости.

В частности, ЛЦИЕ пытается изолировать фрейм Windows Internet Explorer и его вкладки в отдельных процессах. В Windows Internet Explorer 8 такая изоляция повышает производительность и масштабируемость. Это изменение архитектуры может повлиять на совместимость расширений и надстроек, включая элементы управления ActiveX, вспомогательные объекты браузера (BHO) и компоненты панели инструментов пользовательского интерфейса, созданные с помощью старых методов программирования.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Разработка обновлений, влияющих на совместимость браузеров](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



