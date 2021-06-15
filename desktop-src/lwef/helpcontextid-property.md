---
title: Свойство Хелпконтекстид (объект коллекции Commands)
description: Сведения о свойстве Хелпконтекстид объекта коллекции Commands. Microsoft Agent является устаревшим в Windows 7.
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ed6ccf40545e15b3603ce5abe80ef94ff4272a
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068240"
---
# <a name="helpcontextid-property-commands-collection-object"></a><span data-ttu-id="6ef16-104">Свойство Хелпконтекстид (объект коллекции Commands)</span><span class="sxs-lookup"><span data-stu-id="6ef16-104">HelpContextID Property (Commands Collection Object)</span></span>

<span data-ttu-id="6ef16-105">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6ef16-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6ef16-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="6ef16-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6ef16-107">Возвращает или задает связанный контекстный номер для объекта [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="6ef16-107">Returns or sets an associated context number for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="6ef16-108">Используется для предоставления контекстной справки для объекта **Commands** .</span><span class="sxs-lookup"><span data-stu-id="6ef16-108">Used to provide context-sensitive Help for the **Commands** object.</span></span>

</dd> <dt>

<span data-ttu-id="6ef16-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="6ef16-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6ef16-110">\*Символы Agent. \***("**_чарактерид_*_"). Команды ("_*_имя_\*_")._ \*  \[  =  *Номер* хелпконтекстид\]</span><span class="sxs-lookup"><span data-stu-id="6ef16-110">*agent.\***Characters("**_CharacterID_*_").Commands("_*_name_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="6ef16-111">Часть</span><span class="sxs-lookup"><span data-stu-id="6ef16-111">Part</span></span>     | <span data-ttu-id="6ef16-112">Описание</span><span class="sxs-lookup"><span data-stu-id="6ef16-112">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="6ef16-113">*Число*</span><span class="sxs-lookup"><span data-stu-id="6ef16-113">*Number*</span></span> | <span data-ttu-id="6ef16-114">Целое число, указывающее допустимый контекстный номер.</span><span class="sxs-lookup"><span data-stu-id="6ef16-114">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ef16-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="6ef16-115">Remarks</span></span>

<span data-ttu-id="6ef16-116">Если для приложения был создан файл справки Windows и задано свойство [**HelpFile**](helpfile-property.md) символа, агент автоматически вызывает справку, когда [**Хелпмодеон**](helpmodeon-property.md) имеет значение **true** и пользователь выбирает объект [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="6ef16-116">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="6ef16-117">Если задать номер контекста в **хелпконтекстид**, агент вызывает справку и ищет раздел, определяемый этим номером контекста.</span><span class="sxs-lookup"><span data-stu-id="6ef16-117">If you set a context number in the **HelpContextID**, Agent calls Help and searches for the topic identified by that context number.</span></span>

<span data-ttu-id="6ef16-118">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="6ef16-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="6ef16-119">Для создания файла справки требуется компилятор справки Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6ef16-119">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="6ef16-120">См. также</span><span class="sxs-lookup"><span data-stu-id="6ef16-120">See Also</span></span>

[<span data-ttu-id="6ef16-121">**HelpFile, свойство**</span><span class="sxs-lookup"><span data-stu-id="6ef16-121">**HelpFile property**</span></span>](helpfile-property.md)


 

 
