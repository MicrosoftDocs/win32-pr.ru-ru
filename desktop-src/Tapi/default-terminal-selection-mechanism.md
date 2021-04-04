---
description: Понятие терминала с несколькими дорожками делает еще более предпочтительным для TAPI предоставление упрощенного метода выбора терминала в потоке или потоки. Механизм выбора терминала по умолчанию предназначен для решения этой этой программы.
ms.assetid: fbdc7359-b44e-4605-baea-eef5155340c7
title: Механизм выбора терминала по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5512797434fac028e91bf64a88bb9a22b8968c87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897022"
---
# <a name="default-terminal-selection-mechanism"></a>Механизм выбора терминала по умолчанию

Понятие терминала с несколькими [дорожками](multitrack-terminals.md) делает еще более предпочтительным для TAPI предоставление упрощенного метода выбора терминала в потоке или потоки. Механизм выбора терминала по умолчанию предназначен для решения этой этой программы.

## <a name="selecting-a-terminal-on-a-call"></a>Выбор терминала при вызове

Функция выбора терминала по умолчанию предоставляется посредством возможности выбора терминала при вызове.

[Объект call](call-object.md) предоставляет новый интерфейс [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2). Интерфейс предоставляет те же методы, что и [**итбасиккаллконтрол**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol), а также три новых метода: [**рекуесттерминал**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-requestterminal), [**селекттерминалонкалл**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall)и [**унселекттерминалонкалл**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall).

**ITBasicCallControl2:: рекуесттерминал** создает терминал с учетом класса терминала, направления и типа носителя. Он просматривает списки поддерживаемых статических и динамических терминалов для поиска и создания запрошенного терминала.

[**ITBasicCallControl2:: селекттерминалонкалл**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) выбирает терминал (или, в случае многодорожкного терминала, перечисляет, создает при необходимости и выбирает терминалы мониторинга) в потоке (или потоках), доступном при вызове.

Алгоритм сопоставления потоков вызова с терминалом (или дорожками, доступными в терминале) описан в документации по [**ITBasicCallControl2:: селекттерминалонкалл**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall).

Вызов [**ITBasicCallControl2:: унселекттерминалонкалл**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall) приводит к тому, что терминал (одиночная или многодорожкная) будет отделяться от вызова. Дополнительные сведения см. в документации по методу.

## <a name="selecting-a-terminal-on-itstream"></a>Выбор терминала в Итстреам

Выбор терминала с одной дорожкой в [**итстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) (путем вызова [**Итстреам:: селекттерминал**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal)) выбирает терминал в потоке. Это обычная процедура выбора терминала TAPI 3.

В потоке можно выбрать только терминалы с одной дорожкой. Выбор терминала с многодорожкностью в потоке завершится ошибкой, так как поток не сможет распознать тип и направление мультимедиа.

 

 
