---
title: Иаженткоммандсекс Жетглобалвоицекоммандсенаблед
description: Иаженткоммандсекс Жетглобалвоицекоммандсенаблед
ms.assetid: 9c8fa978-a02b-4dfc-8cf7-e066c5b75122
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7275bfe28190e06782cb2564dbf4868dd2c096
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412883"
---
# <a name="iagentcommandsexgetglobalvoicecommandsenabled"></a><span data-ttu-id="e244e-103">Иаженткоммандсекс:: Жетглобалвоицекоммандсенаблед</span><span class="sxs-lookup"><span data-stu-id="e244e-103">IAgentCommandsEx::GetGlobalVoiceCommandsEnabled</span></span>

<span data-ttu-id="e244e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e244e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetGlobalVoiceCommandsEnabled(
   long * pbEnabled  // address of the global voice command setting
);
```

<span data-ttu-id="e244e-105">Возвращает значение, указывающее, включена ли грамматика голоса для глобальных команд агента.</span><span class="sxs-lookup"><span data-stu-id="e244e-105">Retrieves whether the voice grammar for Agent's global commands is enabled.</span></span>

-   <span data-ttu-id="e244e-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e244e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e244e-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*пбенаблед*</span><span class="sxs-lookup"><span data-stu-id="e244e-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="e244e-108">Адрес, который получает **значение true** , если включена грамматика голоса для глобальных команд агента, **значение false** , если отключено.</span><span class="sxs-lookup"><span data-stu-id="e244e-108">The address that receives **True** if the voice grammar for Agent's global commands is enabled, **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="e244e-109">Microsoft Agent автоматически добавляет параметры голоса (грамматики) для открытия и закрытия окна "Voice Commands", а также для отображения и скрытия символа.</span><span class="sxs-lookup"><span data-stu-id="e244e-109">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="e244e-110">Когда этот метод возвращает **значение false**, все параметры голоса для этих команд, а также параметры голоса для [**заголовка**](caption-property.md) объектов [**команд**](/windows/desktop/lwef/the-command-object) других клиентов не включаются в грамматику.</span><span class="sxs-lookup"><span data-stu-id="e244e-110">When this method returns **False**, any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other clients' [**Command**](/windows/desktop/lwef/the-command-object) objects are not included in the grammar.</span></span> <span data-ttu-id="e244e-111">Это позволяет исключить их из текущей активной грамматики клиента.</span><span class="sxs-lookup"><span data-stu-id="e244e-111">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="e244e-112">Однако этот параметр не отражает включение этих команд во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="e244e-112">However, this setting does not reflect the inclusion of these commands in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="e244e-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="e244e-113">See Also</span></span>

[<span data-ttu-id="e244e-114">**Иаженткоммандсекс:: Сетглобалвоицекоммандсенаблед**</span><span class="sxs-lookup"><span data-stu-id="e244e-114">**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**</span></span>](iagentcommandsex--setglobalvoicecommandsenabled.md)


 

 