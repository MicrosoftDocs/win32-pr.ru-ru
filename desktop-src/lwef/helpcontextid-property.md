---
title: Свойство Хелпконтекстид (объект коллекции Commands)
description: Хелпконтекстид, свойство
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d530a1563080108ef2a2798589519ecca03416
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488814"
---
# <a name="helpcontextid-property-commands-collection-object"></a><span data-ttu-id="f03c1-103">Свойство Хелпконтекстид (объект коллекции Commands)</span><span class="sxs-lookup"><span data-stu-id="f03c1-103">HelpContextID Property (Commands Collection Object)</span></span>

<span data-ttu-id="f03c1-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f03c1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f03c1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="f03c1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f03c1-106">Возвращает или задает связанный контекстный номер для объекта [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="f03c1-106">Returns or sets an associated context number for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="f03c1-107">Используется для предоставления контекстной справки для объекта **Commands** .</span><span class="sxs-lookup"><span data-stu-id="f03c1-107">Used to provide context-sensitive Help for the **Commands** object.</span></span>

</dd> <dt>

<span data-ttu-id="f03c1-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="f03c1-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f03c1-109">\*Символы Agent. \***("**_чарактерид_*_"). Команды ("_*_имя_\*_")._ \*  \[  =  *Номер* хелпконтекстид\]</span><span class="sxs-lookup"><span data-stu-id="f03c1-109">*agent.\***Characters("**_CharacterID_*_").Commands("_*_name_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="f03c1-110">Отделение</span><span class="sxs-lookup"><span data-stu-id="f03c1-110">Part</span></span>     | <span data-ttu-id="f03c1-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f03c1-111">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="f03c1-112">*Число*</span><span class="sxs-lookup"><span data-stu-id="f03c1-112">*Number*</span></span> | <span data-ttu-id="f03c1-113">Целое число, указывающее допустимый контекстный номер.</span><span class="sxs-lookup"><span data-stu-id="f03c1-113">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f03c1-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f03c1-114">Remarks</span></span>

<span data-ttu-id="f03c1-115">Если для приложения был создан файл справки Windows и задано свойство [**HelpFile**](helpfile-property.md) символа, агент автоматически вызывает справку, когда [**Хелпмодеон**](helpmodeon-property.md) имеет значение **true** и пользователь выбирает объект [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="f03c1-115">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="f03c1-116">Если задать номер контекста в **хелпконтекстид**, агент вызывает справку и ищет раздел, определяемый этим номером контекста.</span><span class="sxs-lookup"><span data-stu-id="f03c1-116">If you set a context number in the **HelpContextID**, Agent calls Help and searches for the topic identified by that context number.</span></span>

<span data-ttu-id="f03c1-117">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="f03c1-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="f03c1-118">Для создания файла справки требуется компилятор справки Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f03c1-118">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="f03c1-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="f03c1-119">See Also</span></span>

[<span data-ttu-id="f03c1-120">**HelpFile, свойство**</span><span class="sxs-lookup"><span data-stu-id="f03c1-120">**HelpFile property**</span></span>](helpfile-property.md)


 

 
