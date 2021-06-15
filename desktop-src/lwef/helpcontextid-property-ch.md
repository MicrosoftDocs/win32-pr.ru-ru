---
title: Свойство Хелпконтекстид (объект characters)
description: Сведения о свойстве Хелпконтекстид объекта Characters. Microsoft Agent является устаревшим в Windows 7.
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e751cb2d8834a6af2c3b816066d6051e3a28c767
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068190"
---
# <a name="helpcontextid-property-characters-object"></a><span data-ttu-id="6d371-104">Свойство Хелпконтекстид (объект characters)</span><span class="sxs-lookup"><span data-stu-id="6d371-104">HelpContextID Property (Characters Object)</span></span>

<span data-ttu-id="6d371-105">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6d371-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6d371-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="6d371-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6d371-107">Возвращает или задает связанный контекстный номер для символа.</span><span class="sxs-lookup"><span data-stu-id="6d371-107">Returns or sets an associated context number for the character.</span></span> <span data-ttu-id="6d371-108">Используется для предоставления контекстной справки для символа.</span><span class="sxs-lookup"><span data-stu-id="6d371-108">Used to provide context-sensitive Help for the character.</span></span>

</dd> <dt>

<span data-ttu-id="6d371-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="6d371-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6d371-110">\*Символы Agent. \***("**_чарактерид_\*_")._ \*  \[  =  *Номер* хелпконтекстид\]</span><span class="sxs-lookup"><span data-stu-id="6d371-110">*agent.\***Characters("**_CharacterID_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="6d371-111">Часть</span><span class="sxs-lookup"><span data-stu-id="6d371-111">Part</span></span>     | <span data-ttu-id="6d371-112">Описание</span><span class="sxs-lookup"><span data-stu-id="6d371-112">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="6d371-113">*Число*</span><span class="sxs-lookup"><span data-stu-id="6d371-113">*Number*</span></span> | <span data-ttu-id="6d371-114">Целое число, указывающее допустимый контекстный номер.</span><span class="sxs-lookup"><span data-stu-id="6d371-114">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d371-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="6d371-115">Remarks</span></span>

<span data-ttu-id="6d371-116">Для поддержки контекстной справки для символа назначьте номер контекста символу, который используется для связанного раздела справки при компиляции файла справки.</span><span class="sxs-lookup"><span data-stu-id="6d371-116">To support context-sensitive Help for the character, assign the context number to the character you use for the associated Help topic when you compile your Help file.</span></span> <span data-ttu-id="6d371-117">Это свойство применяется только к клиенту символа. параметр не влияет на других клиентов символа или других символов клиента.</span><span class="sxs-lookup"><span data-stu-id="6d371-117">This property applies only to the client of the character; the setting does not affect other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="6d371-118">Если для приложения был создан файл справки Windows и задано свойство [**HelpFile**](helpfile-property.md) символа, агент автоматически вызывает справку, когда [**Хелпмодеон**](helpmodeon-property.md) имеет значение **true** и пользователь щелкает символ.</span><span class="sxs-lookup"><span data-stu-id="6d371-118">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character.</span></span> <span data-ttu-id="6d371-119">Если в [**хелпконтекстид**](helpcontextid-property.md)имеется контекстный номер, агент вызывает справку и ищет раздел, определяемый текущим контекстным номером.</span><span class="sxs-lookup"><span data-stu-id="6d371-119">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="6d371-120">Текущий контекстный номер — это значение **хелпконтекстид** для символа.</span><span class="sxs-lookup"><span data-stu-id="6d371-120">The current context number is the value of **HelpContextID** for the character.</span></span>

> [!Note]  
> <span data-ttu-id="6d371-121">Для создания файла справки требуется компилятор справки Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6d371-121">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="6d371-122">См. также</span><span class="sxs-lookup"><span data-stu-id="6d371-122">See Also</span></span>

[<span data-ttu-id="6d371-123">**HelpFile, свойство**</span><span class="sxs-lookup"><span data-stu-id="6d371-123">**HelpFile property**</span></span>](helpfile-property.md)


 

 




