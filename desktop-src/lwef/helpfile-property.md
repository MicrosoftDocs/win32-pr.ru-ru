---
title: HelpFile, свойство
description: HelpFile, свойство
ms.assetid: 18a5fd9b-4ca7-4701-9993-1e0c55f6e232
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d5307abfba0f884261f5b4a21131a75cf87224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776457"
---
# <a name="helpfile-property"></a><span data-ttu-id="13a8d-103">HelpFile, свойство</span><span class="sxs-lookup"><span data-stu-id="13a8d-103">HelpFile Property</span></span>

<span data-ttu-id="13a8d-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="13a8d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="13a8d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="13a8d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="13a8d-106">Возвращает или задает путь и имя файла справки, зависящей от контекста Microsoft Windows, предоставляемой клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="13a8d-106">Returns or sets the path and filename for a Microsoft Windows context-sensitive Help file supplied by the client application.</span></span>

</dd> <dt>

<span data-ttu-id="13a8d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="13a8d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="13a8d-108">\*агент. ***Символы ("*** чарактерид \* \* *").* \*  \[  =  *Имя файла* HelpFile\]</span><span class="sxs-lookup"><span data-stu-id="13a8d-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Helpfile** \[ = *Filename*\]</span></span>



| <span data-ttu-id="13a8d-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="13a8d-109">Part</span></span>       | <span data-ttu-id="13a8d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="13a8d-110">Description</span></span>                                                                    |
|------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="13a8d-111">*Имя файла*</span><span class="sxs-lookup"><span data-stu-id="13a8d-111">*Filename*</span></span> | <span data-ttu-id="13a8d-112">Строковое выражение, задающее путь и имя файла справки Windows.</span><span class="sxs-lookup"><span data-stu-id="13a8d-112">A string expression specifying the path and filename of the Windows Help file.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13a8d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13a8d-113">Remarks</span></span>

<span data-ttu-id="13a8d-114">Если для приложения был создан файл справки Windows и задано свойство **HelpFile** символа, агент автоматически вызывает справку, когда [**Хелпмодеон**](helpmodeon-property.md) имеет значение **true** , а пользователь щелкает символ или выбирает команду во всплывающем меню.</span><span class="sxs-lookup"><span data-stu-id="13a8d-114">If you've created a Windows Help file for your application and set the character's **HelpFile** property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character or selects a command from its pop-up menu.</span></span> <span data-ttu-id="13a8d-115">Если вы указали контекстный номер в свойстве [**хелпконтекстид**](helpcontextid-property.md) выбранной команды, в справке отображается раздел, соответствующий текущему контексту справки. в противном случае отображается сообщение "нет раздела справки, связанного с этим элементом".</span><span class="sxs-lookup"><span data-stu-id="13a8d-115">If you specified a context number in the [**HelpContextID**](helpcontextid-property.md) property of the selected command, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="13a8d-116">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="13a8d-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="13a8d-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="13a8d-117">See Also</span></span>

<span data-ttu-id="13a8d-118">[**Свойство хелпмодеон**](helpmodeon-property.md), [ **свойство хелпконтекстид**](helpcontextid-property.md)</span><span class="sxs-lookup"><span data-stu-id="13a8d-118">[**HelpModeOn property**](helpmodeon-property.md), [**HelpContextID property**](helpcontextid-property.md)</span></span>


 

 




