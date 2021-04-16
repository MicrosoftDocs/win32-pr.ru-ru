---
title: Свойство Хелпконтекстид (объект characters)
description: Хелпконтекстид, свойство
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42006f74cc3668f8df9af2c2ffcd2515614ec735
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414501"
---
# <a name="helpcontextid-property-characters-object"></a><span data-ttu-id="605a3-103">Свойство Хелпконтекстид (объект characters)</span><span class="sxs-lookup"><span data-stu-id="605a3-103">HelpContextID Property (Characters Object)</span></span>

<span data-ttu-id="605a3-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="605a3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="605a3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="605a3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="605a3-106">Возвращает или задает связанный контекстный номер для символа.</span><span class="sxs-lookup"><span data-stu-id="605a3-106">Returns or sets an associated context number for the character.</span></span> <span data-ttu-id="605a3-107">Используется для предоставления контекстной справки для символа.</span><span class="sxs-lookup"><span data-stu-id="605a3-107">Used to provide context-sensitive Help for the character.</span></span>

</dd> <dt>

<span data-ttu-id="605a3-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="605a3-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="605a3-109">\*Символы Agent. \***("**_чарактерид_\*_")._ \*  \[  =  *Номер* хелпконтекстид\]</span><span class="sxs-lookup"><span data-stu-id="605a3-109">*agent.\***Characters("**_CharacterID_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="605a3-110">Отделение</span><span class="sxs-lookup"><span data-stu-id="605a3-110">Part</span></span>     | <span data-ttu-id="605a3-111">Описание</span><span class="sxs-lookup"><span data-stu-id="605a3-111">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="605a3-112">*Число*</span><span class="sxs-lookup"><span data-stu-id="605a3-112">*Number*</span></span> | <span data-ttu-id="605a3-113">Целое число, указывающее допустимый контекстный номер.</span><span class="sxs-lookup"><span data-stu-id="605a3-113">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="605a3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="605a3-114">Remarks</span></span>

<span data-ttu-id="605a3-115">Для поддержки контекстной справки для символа назначьте номер контекста символу, который используется для связанного раздела справки при компиляции файла справки.</span><span class="sxs-lookup"><span data-stu-id="605a3-115">To support context-sensitive Help for the character, assign the context number to the character you use for the associated Help topic when you compile your Help file.</span></span> <span data-ttu-id="605a3-116">Это свойство применяется только к клиенту символа. параметр не влияет на других клиентов символа или других символов клиента.</span><span class="sxs-lookup"><span data-stu-id="605a3-116">This property applies only to the client of the character; the setting does not affect other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="605a3-117">Если для приложения был создан файл справки Windows и задано свойство [**HelpFile**](helpfile-property.md) символа, агент автоматически вызывает справку, когда [**Хелпмодеон**](helpmodeon-property.md) имеет значение **true** и пользователь щелкает символ.</span><span class="sxs-lookup"><span data-stu-id="605a3-117">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character.</span></span> <span data-ttu-id="605a3-118">Если в [**хелпконтекстид**](helpcontextid-property.md)имеется контекстный номер, агент вызывает справку и ищет раздел, определяемый текущим контекстным номером.</span><span class="sxs-lookup"><span data-stu-id="605a3-118">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="605a3-119">Текущий контекстный номер — это значение **хелпконтекстид** для символа.</span><span class="sxs-lookup"><span data-stu-id="605a3-119">The current context number is the value of **HelpContextID** for the character.</span></span>

> [!Note]  
> <span data-ttu-id="605a3-120">Для создания файла справки требуется компилятор справки Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="605a3-120">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="605a3-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="605a3-121">See Also</span></span>

[<span data-ttu-id="605a3-122">**HelpFile, свойство**</span><span class="sxs-lookup"><span data-stu-id="605a3-122">**HelpFile property**</span></span>](helpfile-property.md)


 

 




