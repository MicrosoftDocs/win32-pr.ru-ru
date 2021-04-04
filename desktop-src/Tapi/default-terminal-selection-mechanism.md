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
# <a name="default-terminal-selection-mechanism"></a><span data-ttu-id="132cb-104">Механизм выбора терминала по умолчанию</span><span class="sxs-lookup"><span data-stu-id="132cb-104">Default Terminal Selection Mechanism</span></span>

<span data-ttu-id="132cb-105">Понятие терминала с несколькими [дорожками](multitrack-terminals.md) делает еще более предпочтительным для TAPI предоставление упрощенного метода выбора терминала в потоке или потоки.</span><span class="sxs-lookup"><span data-stu-id="132cb-105">The concept of [multitrack terminal](multitrack-terminals.md) makes it even more desirable for TAPI to provide a simplified method of selecting a terminal on a stream or streams.</span></span> <span data-ttu-id="132cb-106">Механизм выбора терминала по умолчанию предназначен для решения этой этой программы.</span><span class="sxs-lookup"><span data-stu-id="132cb-106">The Default Terminal Selection mechanism is designed to address this.</span></span>

## <a name="selecting-a-terminal-on-a-call"></a><span data-ttu-id="132cb-107">Выбор терминала при вызове</span><span class="sxs-lookup"><span data-stu-id="132cb-107">Selecting a Terminal on a Call</span></span>

<span data-ttu-id="132cb-108">Функция выбора терминала по умолчанию предоставляется посредством возможности выбора терминала при вызове.</span><span class="sxs-lookup"><span data-stu-id="132cb-108">The Default Terminal Selection feature is provided via the ability to select a terminal on a call.</span></span>

<span data-ttu-id="132cb-109">[Объект call](call-object.md) предоставляет новый интерфейс [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2).</span><span class="sxs-lookup"><span data-stu-id="132cb-109">The [call object](call-object.md) exposes a new interface, [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2).</span></span> <span data-ttu-id="132cb-110">Интерфейс предоставляет те же методы, что и [**итбасиккаллконтрол**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol), а также три новых метода: [**рекуесттерминал**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-requestterminal), [**селекттерминалонкалл**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall)и [**унселекттерминалонкалл**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall).</span><span class="sxs-lookup"><span data-stu-id="132cb-110">The interface exposes the same methods as [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol), plus three new methods: [**RequestTerminal**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-requestterminal), [**SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall), and [**UnselectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall).</span></span>

<span data-ttu-id="132cb-111">**ITBasicCallControl2:: рекуесттерминал** создает терминал с учетом класса терминала, направления и типа носителя.</span><span class="sxs-lookup"><span data-stu-id="132cb-111">**ITBasicCallControl2::RequestTerminal** creates a terminal, given the terminal class, direction, and media type.</span></span> <span data-ttu-id="132cb-112">Он просматривает списки поддерживаемых статических и динамических терминалов для поиска и создания запрошенного терминала.</span><span class="sxs-lookup"><span data-stu-id="132cb-112">It looks through the lists of supported static and dynamic terminals to find and create the requested terminal.</span></span>

<span data-ttu-id="132cb-113">[**ITBasicCallControl2:: селекттерминалонкалл**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) выбирает терминал (или, в случае многодорожкного терминала, перечисляет, создает при необходимости и выбирает терминалы мониторинга) в потоке (или потоках), доступном при вызове.</span><span class="sxs-lookup"><span data-stu-id="132cb-113">[**ITBasicCallControl2::SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) selects the terminal (or, in the case of a multitrack terminal, enumerates, creates if needed, and selects the track terminals) on the stream (or streams) available on the call.</span></span>

<span data-ttu-id="132cb-114">Алгоритм сопоставления потоков вызова с терминалом (или дорожками, доступными в терминале) описан в документации по [**ITBasicCallControl2:: селекттерминалонкалл**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall).</span><span class="sxs-lookup"><span data-stu-id="132cb-114">The algorithm for matching call streams to the terminal (or tracks available on the terminal) is described in the documentation for [**ITBasicCallControl2::SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall).</span></span>

<span data-ttu-id="132cb-115">Вызов [**ITBasicCallControl2:: унселекттерминалонкалл**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall) приводит к тому, что терминал (одиночная или многодорожкная) будет отделяться от вызова.</span><span class="sxs-lookup"><span data-stu-id="132cb-115">Calling [**ITBasicCallControl2::UnselectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall) causes the terminal (single-track or multitrack) to be unselected from the call.</span></span> <span data-ttu-id="132cb-116">Дополнительные сведения см. в документации по методу.</span><span class="sxs-lookup"><span data-stu-id="132cb-116">See the method's documentation for more details.</span></span>

## <a name="selecting-a-terminal-on-itstream"></a><span data-ttu-id="132cb-117">Выбор терминала в Итстреам</span><span class="sxs-lookup"><span data-stu-id="132cb-117">Selecting a Terminal on ITStream</span></span>

<span data-ttu-id="132cb-118">Выбор терминала с одной дорожкой в [**итстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) (путем вызова [**Итстреам:: селекттерминал**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal)) выбирает терминал в потоке.</span><span class="sxs-lookup"><span data-stu-id="132cb-118">Selecting a single-track terminal on [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) (by calling [**ITStream::SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal)) selects the terminal on the stream.</span></span> <span data-ttu-id="132cb-119">Это обычная процедура выбора терминала TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="132cb-119">This is the usual TAPI 3 terminal selection procedure.</span></span>

<span data-ttu-id="132cb-120">В потоке можно выбрать только терминалы с одной дорожкой.</span><span class="sxs-lookup"><span data-stu-id="132cb-120">Only single-tracks terminals can be selected on a stream.</span></span> <span data-ttu-id="132cb-121">Выбор терминала с многодорожкностью в потоке завершится ошибкой, так как поток не сможет распознать тип и направление мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="132cb-121">Selecting a multitrack terminal on a stream will fail, because the stream will not recognize the media type and direction.</span></span>

 

 
