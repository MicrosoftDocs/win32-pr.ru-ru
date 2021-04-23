---
title: Свойство FontName (объект всплывающего объекта)
description: FontName, свойство
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead06323b36e86dce36163769b329140279f240d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134967"
---
# <a name="fontname-property-balloon-object"></a><span data-ttu-id="9e419-103">Свойство FontName (объект всплывающего объекта)</span><span class="sxs-lookup"><span data-stu-id="9e419-103">FontName Property (Balloon Object)</span></span>

<span data-ttu-id="9e419-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9e419-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9e419-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="9e419-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9e419-106">Возвращает или задает шрифт, используемый в подсказке слова для указанного символа.</span><span class="sxs-lookup"><span data-stu-id="9e419-106">Returns or sets the font used in the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="9e419-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="9e419-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9e419-108">\*Символы Agent. \***("**_чарактерид_\*_"). Шрифт выноски. FontName_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="9e419-108">*agent.\***Characters("**_CharacterID_*_").Balloon.FontName_\* \[ = *font*\]</span></span>



| <span data-ttu-id="9e419-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="9e419-109">Part</span></span>   | <span data-ttu-id="9e419-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9e419-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="9e419-111">*шрифтов*</span><span class="sxs-lookup"><span data-stu-id="9e419-111">*font*</span></span> | <span data-ttu-id="9e419-112">Строковое значение, соответствующее имени шрифта.</span><span class="sxs-lookup"><span data-stu-id="9e419-112">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e419-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e419-113">Remarks</span></span>

<span data-ttu-id="9e419-114">Свойство [**FontName**](fontname-property.md) определяет шрифт, используемый для отображения текста в окне всплывающей подсказки в слове строки.</span><span class="sxs-lookup"><span data-stu-id="9e419-114">The [**FontName**](fontname-property.md) property defines the font used to display text in the word balloon window of a string.</span></span> <span data-ttu-id="9e419-115">Значение по умолчанию для параметров шрифта всплывающей подсказки для символа задается в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="9e419-115">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="9e419-116">Кроме того, пользователь может переопределить параметры шрифта для всех символов на странице свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="9e419-116">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="9e419-117">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="9e419-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="9e419-118">Если вы используете некомпилированный символ, проверьте свойства [**FontName**](fontname-property.md) и [**фонтчарсет**](fontcharset-property.md) для символа, чтобы определить, подходит ли он для вашего языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="9e419-118">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and [**FontCharSet**](fontcharset-property.md) properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="9e419-119">Возможно, потребуется задать эти значения перед использованием метода [**говорите**](speak-method.md) , чтобы обеспечить отображение текста в выноске слова.</span><span class="sxs-lookup"><span data-stu-id="9e419-119">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 




