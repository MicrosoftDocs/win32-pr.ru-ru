---
title: Метод обработки
description: Метод обработки
ms.assetid: a188dd47-6af1-429d-af0a-69451f6b495e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a896c499e11aeaf50bfe9adc82a8330e61fc693
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890549"
---
# <a name="think-method"></a><span data-ttu-id="f52d3-103">Метод обработки</span><span class="sxs-lookup"><span data-stu-id="f52d3-103">Think Method</span></span>

<span data-ttu-id="f52d3-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f52d3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f52d3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="f52d3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f52d3-106">Отображает указанный текст для указанного символа в всплывающей подсказке слова «мысль».</span><span class="sxs-lookup"><span data-stu-id="f52d3-106">Displays the specified text for the specified character in a "thought" word balloon.</span></span>

</dd> <dt>

<span data-ttu-id="f52d3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="f52d3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f52d3-108">\*Агент ***. Символы ("*** чарактерид \* \* *"). Текст для обдумывания* \*  \[ \]</span><span class="sxs-lookup"><span data-stu-id="f52d3-108">*agent ***.Characters ("*** CharacterID\*\*\*").Think*\* \[*Text*\]</span></span>



| <span data-ttu-id="f52d3-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="f52d3-109">Part</span></span>   | <span data-ttu-id="f52d3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f52d3-110">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="f52d3-111">*Text*</span><span class="sxs-lookup"><span data-stu-id="f52d3-111">*Text*</span></span> | <span data-ttu-id="f52d3-112">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="f52d3-112">Optional.</span></span> <span data-ttu-id="f52d3-113">Строка, указывающая результат мышления символа.</span><span class="sxs-lookup"><span data-stu-id="f52d3-113">A string that specifies the character's thought output.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f52d3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f52d3-114">Remarks</span></span>

<span data-ttu-id="f52d3-115">Как и в случае с методом [**говорите**](speak-method.md) , метод **обработки** — это запрос в очереди, отображающий текст в выноске, за исключением того, что всплывающее сообщение о **подозрении** выглядит иначе.</span><span class="sxs-lookup"><span data-stu-id="f52d3-115">Like the [**Speak**](speak-method.md) method, the **Think** method is a queued request that displays text in a word balloon, except that the **Think** word balloon differs visually.</span></span> <span data-ttu-id="f52d3-116">Кроме того, всплывающее подсказка поддерживает только тег элемента управления речью в закладке (**\\ МРК**) и игнорирует все другие теги элементов управления речевыми функциями.</span><span class="sxs-lookup"><span data-stu-id="f52d3-116">In addition, the balloon supports only the Bookmark speech control tag (**\\Mrk**) and ignores any other speech control tags.</span></span> <span data-ttu-id="f52d3-117">В отличие от **говорите**, метод **обработки** не изменяет состояние анимации символа.</span><span class="sxs-lookup"><span data-stu-id="f52d3-117">Unlike **Speak**, the **Think** method does not change the character's animation state.</span></span>

<span data-ttu-id="f52d3-118">Свойства [**всплывающего**](/windows/desktop/lwef/the-balloon-object) объекта влияют на выходные данные методов [**произношения**](speak-method.md) и **обработки** .</span><span class="sxs-lookup"><span data-stu-id="f52d3-118">The [**Balloon**](/windows/desktop/lwef/the-balloon-object) object's properties affect the output of both the [**Speak**](speak-method.md) and **Think** methods.</span></span> <span data-ttu-id="f52d3-119">Например, для отображения текста свойство [**Enabled**](enabled-property.md) объекта **всплывающего** окна должно иметь **значение true** .</span><span class="sxs-lookup"><span data-stu-id="f52d3-119">For example, the **Balloon** object's [**Enabled**](enabled-property.md) property must be **True** for text to display.</span></span>

<span data-ttu-id="f52d3-120">Если объявляется ссылка на объект и устанавливается этот метод, он возвращает объект [**запроса**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="f52d3-120">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="f52d3-121">Кроме того, если файл не был загружен, сервер устанавливает для свойства [**Status**](status-property.md) объекта **запроса** значение "сбой" с соответствующим номером кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="f52d3-121">In addition, if the file has not been loaded, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error code number.</span></span>

<span data-ttu-id="f52d3-122">Автоматическое разбиение слов агента в выноске обрывает слова, используя пробелы (например, пробел или знак табуляции).</span><span class="sxs-lookup"><span data-stu-id="f52d3-122">Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, Space or Tab).</span></span> <span data-ttu-id="f52d3-123">Однако, если это невозможно, может нарушиться слово, чтобы уместить всплывающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="f52d3-123">However, if it cannot, it may break a word to fit the balloon.</span></span> <span data-ttu-id="f52d3-124">В таких языках, как японский, китайский и тайский, где пробелы не используются для разбиения слов, вставьте символ пробела нулевой ширины (0x200B) в Юникоде между символами, чтобы определить логические разрывы слов.</span><span class="sxs-lookup"><span data-stu-id="f52d3-124">In languages like Japanese, Chinese, and Thai where spaces are not used to break words, insert a Unicode zero-width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="f52d3-125">Перед тем как использовать метод [**говорите**](speak-method.md) для отображения текста внутри всплывающей подсказки, задайте идентификатор языка символа.</span><span class="sxs-lookup"><span data-stu-id="f52d3-125">Set the character's language ID before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 