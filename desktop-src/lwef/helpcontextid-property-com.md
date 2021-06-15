---
title: Свойство Хелпконтекстид (объект Command)
description: Сведения о свойстве Хелпконтекстид объекта Command. Microsoft Agent является устаревшим в Windows 7.
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461c3c0ff5a6722dd6740c7df7e89bf2b9520053
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068518"
---
# <a name="helpcontextid-property-command-object"></a><span data-ttu-id="5458a-104">Свойство Хелпконтекстид (объект Command)</span><span class="sxs-lookup"><span data-stu-id="5458a-104">HelpContextID Property (Command Object)</span></span>

<span data-ttu-id="5458a-105">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5458a-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5458a-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="5458a-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5458a-107">Возвращает или задает связанный контекстный номер для объекта [**команды**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="5458a-107">Returns or sets an associated context number for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="5458a-108">Используется для предоставления контекстной справки для объекта **Command** .</span><span class="sxs-lookup"><span data-stu-id="5458a-108">Used to provide context-sensitive Help for the **Command** object.</span></span>

</dd> <dt>

<span data-ttu-id="5458a-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="5458a-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5458a-110">\*Символы Agent. \***("**_чарактерид_\*_"). Команды ("")._ \*  \[  =  *Номер* хелпконтекстид\]</span><span class="sxs-lookup"><span data-stu-id="5458a-110">*agent.\***Characters("**_CharacterID_*_").Commands("").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="5458a-111">Часть</span><span class="sxs-lookup"><span data-stu-id="5458a-111">Part</span></span>     | <span data-ttu-id="5458a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5458a-112">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="5458a-113">*Число*</span><span class="sxs-lookup"><span data-stu-id="5458a-113">*Number*</span></span> | <span data-ttu-id="5458a-114">Целое число, указывающее допустимый контекстный номер.</span><span class="sxs-lookup"><span data-stu-id="5458a-114">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5458a-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="5458a-115">Remarks</span></span>

<span data-ttu-id="5458a-116">Если вы создали файл справки Windows для приложения и присвойте файлу свойство [**HelpFile**](helpfile-property.md) символа, агент автоматически вызывает справку, когда [**Хелпмодеон**](helpmodeon-property.md) имеет значение **true** и пользователь выбирает команду.</span><span class="sxs-lookup"><span data-stu-id="5458a-116">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property to the file, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="5458a-117">Если задать номер контекста в [**хелпконтекстид**](helpcontextid-property.md), агент вызывает справку и ищет раздел, определяемый текущим контекстным номером.</span><span class="sxs-lookup"><span data-stu-id="5458a-117">If you set a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="5458a-118">Текущий контекстный номер — это значение **хелпконтекстид** для команды.</span><span class="sxs-lookup"><span data-stu-id="5458a-118">The current context number is the value of **HelpContextID** for the command.</span></span>

<span data-ttu-id="5458a-119">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="5458a-119">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="5458a-120">Для создания файла справки требуется компилятор справки Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5458a-120">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="5458a-121">См. также</span><span class="sxs-lookup"><span data-stu-id="5458a-121">See Also</span></span>

[<span data-ttu-id="5458a-122">**HelpFile, свойство**</span><span class="sxs-lookup"><span data-stu-id="5458a-122">**HelpFile property**</span></span>](helpfile-property.md)


 

 
