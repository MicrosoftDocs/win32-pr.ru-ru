---
title: исан
description: Атрибут ИСАН содержит номер Международной стандартной аудиовизуального (ИСАН), определяющий содержимое.
ms.assetid: 2937d422-f062-4373-845e-dd200512ed0b
keywords:
- Формат Windows Media ИСАН
topic_type:
- apiref
api_name:
- ISAN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dc4a850edc43178deb043143ee8f9b37140507
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104412609"
---
# <a name="isan"></a><span data-ttu-id="9d53e-104">исан</span><span class="sxs-lookup"><span data-stu-id="9d53e-104">ISAN</span></span>

<span data-ttu-id="9d53e-105">Атрибут **Исан** содержит номер Международной стандартной АУДИОВИЗУАЛЬНОГО (Исан), определяющий содержимое.</span><span class="sxs-lookup"><span data-stu-id="9d53e-105">The **ISAN** attribute contains the International Standard Audiovisual Number (ISAN) that identifies the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="9d53e-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="9d53e-106">Global Constant</span></span>

<span data-ttu-id="9d53e-107">g \_ всзисан</span><span class="sxs-lookup"><span data-stu-id="9d53e-107">g\_wszISAN</span></span>

## <a name="data-type"></a><span data-ttu-id="9d53e-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9d53e-108">Data Type</span></span>

<span data-ttu-id="9d53e-109">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="9d53e-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="9d53e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d53e-110">Remarks</span></span>

<span data-ttu-id="9d53e-111">ИСАН — это Международный стандарт для идентификации аудиовизуального Works.</span><span class="sxs-lookup"><span data-stu-id="9d53e-111">ISAN is an international standard for identifying audiovisual works.</span></span> <span data-ttu-id="9d53e-112">Сведения о ИСАН см. на [веб-сайте](https://www.isan.org/)Standard.</span><span class="sxs-lookup"><span data-stu-id="9d53e-112">For information about ISAN, visit the standard's [Web site](https://www.isan.org/).</span></span>

<span data-ttu-id="9d53e-113">Объект редактора метаданных проверяет строку ИСАН при задании этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="9d53e-113">The metadata editor object verifies the ISAN string when you set this attribute.</span></span> <span data-ttu-id="9d53e-114">Допустимое форматирование строк, как описано в разделе 4,1 спецификации ИСАН, состоит из 16 шестнадцатеричных цифр, которые дополнительно разделяются пробелами или дефисами в 4-значные сегменты.</span><span class="sxs-lookup"><span data-stu-id="9d53e-114">The acceptable string formatting, as described in section 4.1 of the ISAN specification, consists of 16 hexadecimal digits, optionally separated by whitespace or hyphens into 4-digit segments.</span></span> <span data-ttu-id="9d53e-115">Необходимо соблюдать форматированный номер, который также может быть отделен пробелом или дефисом, по допустимому символу Check.</span><span class="sxs-lookup"><span data-stu-id="9d53e-115">The formatted number must be followed, also optionally separated by a space or hyphen, by a valid check character.</span></span> <span data-ttu-id="9d53e-116">Символом проверки может быть десятичная цифра или заглавная буква.</span><span class="sxs-lookup"><span data-stu-id="9d53e-116">The check character can be a decimal digit or a capital letter.</span></span> <span data-ttu-id="9d53e-117">Сведения о том, как получить номер проверки, см. в приложении A из руководства пользователя ИСАН.</span><span class="sxs-lookup"><span data-stu-id="9d53e-117">Refer to annex A of the ISAN user guide for information about how to derive the check number.</span></span>

<span data-ttu-id="9d53e-118">После строки стандартной ИСАН может следовать информация о версии.</span><span class="sxs-lookup"><span data-stu-id="9d53e-118">The standard ISAN string may be followed by version information.</span></span> <span data-ttu-id="9d53e-119">При наличии сведений о версии она состоит из восьми шестнадцатеричных цифр, за которыми следует номер чека.</span><span class="sxs-lookup"><span data-stu-id="9d53e-119">If present, version information consists of eight hexadecimal digits followed by a check number.</span></span> <span data-ttu-id="9d53e-120">Форматирование этих символов следует тем же правилам, что и базовая строка.</span><span class="sxs-lookup"><span data-stu-id="9d53e-120">The formatting of these characters follows the same rules as the basic string.</span></span>

## <a name="examples"></a><span data-ttu-id="9d53e-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="9d53e-121">Examples</span></span>

<span data-ttu-id="9d53e-122">Ниже приведены три приемлемых отформатированных строки для примера ИСАН.</span><span class="sxs-lookup"><span data-stu-id="9d53e-122">The following are three acceptably formatted strings for an example ISAN.</span></span>


```
00003BAB93520000G
0000 3BAB 9352 0000 G
0000-3BAB-9352-0000-G
```



<span data-ttu-id="9d53e-123">Следующая строка показывает формат ИСАН с информацией о версии.</span><span class="sxs-lookup"><span data-stu-id="9d53e-123">The following string shows the format of an ISAN with version information.</span></span>


```C++
0000-3BAB-9352-0000-G-0000-0000-Q
```



## <a name="see-also"></a><span data-ttu-id="9d53e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d53e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d53e-125">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="9d53e-125">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




