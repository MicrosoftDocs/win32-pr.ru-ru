---
title: Иаженткоммандсекс Сетглобалвоицекоммандсенаблед
description: Иаженткоммандсекс Сетглобалвоицекоммандсенаблед
ms.assetid: f456b1d3-60aa-4b90-90d0-6c695947fa8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87a576a36d3df4b3ddf0ca71f5709a712a3c9e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133795"
---
# <a name="iagentcommandsexsetglobalvoicecommandsenabled"></a><span data-ttu-id="58003-103">Иаженткоммандсекс:: Сетглобалвоицекоммандсенаблед</span><span class="sxs-lookup"><span data-stu-id="58003-103">IAgentCommandsEx::SetGlobalVoiceCommandsEnabled</span></span>

<span data-ttu-id="58003-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="58003-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetGlobalVoiceCommandsEnabled(
 long bEnable  // Enabled setting for Agent's global voice commands
);
```

<span data-ttu-id="58003-105">Задает свойство [**Enabled**](enabled-property.md) для грамматики голоса для глобальных команд агента Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="58003-105">Sets the [**Enabled**](enabled-property.md) property for the voice grammar of Microsoft Agent's global commands.</span></span>

-   <span data-ttu-id="58003-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="58003-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="58003-107"><span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*бенабле*</span><span class="sxs-lookup"><span data-stu-id="58003-107"><span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*bEnable*</span></span>
</dt> <dd>

<span data-ttu-id="58003-108">Логическое значение, которое указывает, включена ли грамматика голоса для глобальных команд агента.</span><span class="sxs-lookup"><span data-stu-id="58003-108">A Boolean value that sets whether the voice grammar of Agent's global commands is enabled.</span></span> <span data-ttu-id="58003-109">**Значение true** включает грамматику голоса; **Значение false** отключает его.</span><span class="sxs-lookup"><span data-stu-id="58003-109">**True** enables the voice grammar; **False** disables it.</span></span>

</dd> </dl>

<span data-ttu-id="58003-110">Microsoft Agent автоматически добавляет параметры голоса (грамматики) для открытия и закрытия окна "Voice Commands", а также для отображения и скрытия символа.</span><span class="sxs-lookup"><span data-stu-id="58003-110">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="58003-111">Если задано **значение false**, то агент отключает любые параметры голоса для этих команд, а также параметры голоса для [**заголовка**](caption-property.md) объектов [**команд**](/windows/desktop/lwef/the-command-object) другого клиента.</span><span class="sxs-lookup"><span data-stu-id="58003-111">When set to **False**, Agent disables any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other client's [**Command**](/windows/desktop/lwef/the-command-object) objects.</span></span> <span data-ttu-id="58003-112">Это позволяет исключить их из текущей активной грамматики клиента.</span><span class="sxs-lookup"><span data-stu-id="58003-112">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="58003-113">Однако, так как это потенциально блокирует голосовой доступ к другим клиентам, сбросьте это свойство в **значение true** после обработки речевого ввода пользователя.</span><span class="sxs-lookup"><span data-stu-id="58003-113">However, because this potentially blocks voice access to other clients, reset this property to **True** after processing the user's voice input.</span></span>

<span data-ttu-id="58003-114">Отключение свойства не влияет на всплывающее меню символа.</span><span class="sxs-lookup"><span data-stu-id="58003-114">Disabling the property does not affect the character's pop-up menu.</span></span> <span data-ttu-id="58003-115">Глобальные команды, добавленные сервером, по-прежнему будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="58003-115">The global commands added by the server will still appear.</span></span> <span data-ttu-id="58003-116">Их нельзя удалить из всплывающего меню.</span><span class="sxs-lookup"><span data-stu-id="58003-116">You cannot remove them from the pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="58003-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="58003-117">See Also</span></span>

[<span data-ttu-id="58003-118">**Иаженткоммандсекс:: Жетглобалвоицекоммандсенаблед**</span><span class="sxs-lookup"><span data-stu-id="58003-118">**IAgentCommandsEx::GetGlobalVoiceCommandsEnabled**</span></span>](iagentcommandsex--getglobalvoicecommandsenabled.md)


 

 