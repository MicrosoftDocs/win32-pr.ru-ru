---
title: Клоседкаптион. Самифиленаме
description: Свойство Самифиленаме указывает или получает имя файла, содержащего сведения, необходимые для закрытого субтитров.
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- Проигрыватель Windows Media Клоседкаптион. Самифиленаме
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIFileName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd748076eec80b5b7d97e7c041f454c4f9193f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694874"
---
# <a name="closedcaptionsamifilename"></a><span data-ttu-id="e3062-104">Клоседкаптион. Самифиленаме</span><span class="sxs-lookup"><span data-stu-id="e3062-104">ClosedCaption.SAMIFileName</span></span>

<span data-ttu-id="e3062-105">Свойство **самифиленаме** указывает или получает имя файла, содержащего сведения, необходимые для закрытого субтитров.</span><span class="sxs-lookup"><span data-stu-id="e3062-105">The **SAMIFileName** property specifies or retrieves the name of the file containing the information needed for closed captioning.</span></span>

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a><span data-ttu-id="e3062-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="e3062-106">Possible Values</span></span>

<span data-ttu-id="e3062-107">Это свойство является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e3062-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3062-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3062-108">Remarks</span></span>

<span data-ttu-id="e3062-109">Синхронизированный доступный файл обмена мультимедийными данными (SAMI) должен использовать расширение имени файла. SMI или Sami.</span><span class="sxs-lookup"><span data-stu-id="e3062-109">The Synchronized Accessible Media Interchange (SAMI) file must use an .smi or .sami file name extension.</span></span>

<span data-ttu-id="e3062-110">Если не указать значение для **самифиленаме**, это свойство получает строку, содержащую имя файла или URL-адрес, связанный с текущим элементом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e3062-110">If you don't specify a value for **SAMIFileName**, this property retrieves a string containing the file name or URL associated with the current media item.</span></span> <span data-ttu-id="e3062-111">Такая ассоциация может возникнуть, когда файл SAMI указывается с помощью параметра URL-адреса *Sami* или автоматически, если имя файла Sami совпадает с именем файла цифрового носителя (за исключением расширения имени файла).</span><span class="sxs-lookup"><span data-stu-id="e3062-111">This association can occur when a SAMI file is specified using the *sami* URL parameter, or automatically when the SAMI file has the same name as the digital media file name (except for the file name extension).</span></span> <span data-ttu-id="e3062-112">Если с текущим носителем не связан файл SAMI, это свойство получает пустую строку ("").</span><span class="sxs-lookup"><span data-stu-id="e3062-112">If there is no SAMI file associated with the current media, this property retrieves an empty string ("").</span></span>

<span data-ttu-id="e3062-113">После указания значения для **самифиленаме** это значение сохраняется до тех пор, пока не будет указано новое значение (или до открытия нового элемента мультимедиа с помощью параметра *Sami* URL).</span><span class="sxs-lookup"><span data-stu-id="e3062-113">Once you specify a value for **SAMIFileName**, that value persists until you specify a new value (or until a new media item is opened using the *sami* URL parameter).</span></span> <span data-ttu-id="e3062-114">Поэтому перед воспроизведением каждого нового элемента мультимедиа необходимо указать новое значение для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="e3062-114">Therefore, you must specify a new value for this property before you play each new media item.</span></span> <span data-ttu-id="e3062-115">Таким образом, новое значение для **самифиленаме** вступит в силу при открытии следующего элемента мультимедиа (или *проигрывателя*.\*\*\*\* вызывается Close).</span><span class="sxs-lookup"><span data-stu-id="e3062-115">That way, the new value for **SAMIFileName** will take effect when the next media item is opened (or when *Player*.**close** is called).</span></span> <span data-ttu-id="e3062-116">Указание нового значения для **самифиленаме** не влияет на текущий носитель.</span><span class="sxs-lookup"><span data-stu-id="e3062-116">Specifying a new value for **SAMIFileName** has no effect for the current media.</span></span>

<span data-ttu-id="e3062-117">Чтобы проигрыватель Windows Media возвращался с помощью файла SAMI, связанного с определенным элементом мультимедиа, перед воспроизведением следующего элемента мультимедиа укажите значение **самифиленаме** , равное пустой строке ("").</span><span class="sxs-lookup"><span data-stu-id="e3062-117">To cause Windows Media Player to return to using the SAMI file associated with a particular media item, specify a value for **SAMIFileName** equal to an empty string ("") before you play the next media item.</span></span>

<span data-ttu-id="e3062-118">**Проигрыватель Windows Media 10 Mobile:** Это свойство доступно только для чтения и всегда возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="e3062-118">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="e3062-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="e3062-119">Examples</span></span>

<span data-ttu-id="e3062-120">В следующих трех примерах JScript используется *клоседкаптион*. **Самифиленаме** , чтобы указать имя текстового файла с закрытым заголовком.</span><span class="sxs-lookup"><span data-stu-id="e3062-120">The following three JScript examples use *ClosedCaption*.**SAMIFileName** to specify the name of a closed caption text file.</span></span> <span data-ttu-id="e3062-121">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="e3062-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Display the closed captions from a website.
Player.closedCaption.SAMIFileName="https://www.proseware.com/ccsample.smi";

// Display the closed captions from a local network.
// You must add an escape sequence of a backslash for every original backslash.
Player.closedCaption.SAMIFileName="\\\\yourservername\\Public\\ccsample.smi";

// Display the closed captions from a file on a local drive.
// Be sure to add the appropriate escape sequences.
Player.closedCaption.SAMIFileName="C:\\WMSDK\\WMPSDK9\\samples\\media\\ccsample.smi";

```



## <a name="requirements"></a><span data-ttu-id="e3062-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e3062-122">Requirements</span></span>



| <span data-ttu-id="e3062-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e3062-123">Requirement</span></span> | <span data-ttu-id="e3062-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e3062-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3062-125">Версия</span><span class="sxs-lookup"><span data-stu-id="e3062-125">Version</span></span><br/> | <span data-ttu-id="e3062-126">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="e3062-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e3062-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e3062-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="e3062-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3062-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3062-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3062-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3062-130">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="e3062-130">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="e3062-131">**Объект Клоседкаптион**</span><span class="sxs-lookup"><span data-stu-id="e3062-131">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="e3062-132">**Player. закрыть**</span><span class="sxs-lookup"><span data-stu-id="e3062-132">**Player.close**</span></span>](player-close.md)
</dt> </dl>

 

 





