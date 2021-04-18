---
title: Иаженткоммандсекс Жетвоицекаптион
description: Иаженткоммандсекс Жетвоицекаптион
ms.assetid: 0e505295-386a-421f-a43c-6da03c8a2b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a757e1c841afd62b9b6ae13f1ef34178f133ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105710267"
---
# <a name="iagentcommandsexgetvoicecaption"></a><span data-ttu-id="c698e-103">Иаженткоммандсекс:: Жетвоицекаптион</span><span class="sxs-lookup"><span data-stu-id="c698e-103">IAgentCommandsEx::GetVoiceCaption</span></span>

<span data-ttu-id="c698e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c698e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption
);
```

<span data-ttu-id="c698e-105">Получает [**воицекаптион**](voicecaption-property.md) для объекта [**команды**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="c698e-105">Retrieves the [**VoiceCaption**](voicecaption-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="c698e-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c698e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c698e-107"><span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*пбсзвоицекаптион*</span><span class="sxs-lookup"><span data-stu-id="c698e-107"><span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="c698e-108">Адрес строки BSTR, которая получает значение текста [**заголовка**](caption-property.md) , отображаемого для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="c698e-108">The address of a BSTR that receives the value of the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="c698e-109">Возвращаемый текст определяется для объекта [**команды**](/windows/desktop/lwef/the-command-object) и отображается в окне "команды Voice", если клиентское приложение является входным.</span><span class="sxs-lookup"><span data-stu-id="c698e-109">The text returned is that set for your [**Command**](/windows/desktop/lwef/the-command-object) object and appears in the Voice Commands window when your client application is input-active.</span></span>

<span data-ttu-id="c698e-110">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="c698e-110">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="c698e-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="c698e-111">See Also</span></span>

[<span data-ttu-id="c698e-112">**Иаженткоммандсекс:: Сетвоицекаптион**</span><span class="sxs-lookup"><span data-stu-id="c698e-112">**IAgentCommandsEx::SetVoiceCaption**</span></span>](iagentcommandsex--setvoicecaption.md)


 

 