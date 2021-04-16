---
title: Ивмпклоседкаптион Самифиленаме, свойство
description: Свойство Самифиленаме Возвращает или задает имя файла, содержащего сведения, необходимые для закрытого субтитров.
ms.assetid: c3162c5f-9d66-41d4-920c-ed9840742d9d
keywords:
- Проигрыватель Windows Media для свойства Самифиленаме
- Самифиленаме свойство проигрывателя Windows Media Player, интерфейс Ивмпклоседкаптион
- Интерфейс Ивмпклоседкаптион Windows Media Player, свойство Самифиленаме
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIFileName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251f2bbf0c8839ab9a0005c69e1869c47af16ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648823"
---
# <a name="iwmpclosedcaptionsamifilename-property"></a><span data-ttu-id="11197-106">Свойство Ивмпклоседкаптион:: Самифиленаме</span><span class="sxs-lookup"><span data-stu-id="11197-106">IWMPClosedCaption::SAMIFileName property</span></span>

<span data-ttu-id="11197-107">Свойство **самифиленаме** Возвращает или задает имя файла, содержащего сведения, необходимые для закрытого субтитров.</span><span class="sxs-lookup"><span data-stu-id="11197-107">The **SAMIFileName** property gets or sets the name of a file containing the information needed for closed captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="11197-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11197-108">Syntax</span></span>


```CSharp
public System.String SAMIFileName {get; set;}
```


```VB

Public Property SAMIFileName As System.String
```





## <a name="property-value"></a><span data-ttu-id="11197-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="11197-109">Property value</span></span>

<span data-ttu-id="11197-110">**Строка System. String** , которая является именем синхронизированного доступного файла обмена мультимедиа (SAMI).</span><span class="sxs-lookup"><span data-stu-id="11197-110">The **System.String** that is the name of the Synchronized Accessible Media Interchange (SAMI) file.</span></span>

## <a name="remarks"></a><span data-ttu-id="11197-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11197-111">Remarks</span></span>

<span data-ttu-id="11197-112">Файл SAMI должен иметь расширение имени файла. SMI или Sami.</span><span class="sxs-lookup"><span data-stu-id="11197-112">The SAMI file must use an .smi or .sami file name extension.</span></span>

<span data-ttu-id="11197-113">Если не задать значение с помощью **самифиленаме**, это свойство получает **строку** , содержащую имя файла по умолчанию или URL-адрес, связанный с текущим элементом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="11197-113">If you do not set a value using **SAMIFileName**, this property gets a **string** containing the default file name or URL associated with the current media item.</span></span> <span data-ttu-id="11197-114">Такая ассоциация может возникнуть, когда файл SAMI указывается с помощью параметра URL-адреса *Sami* или автоматически, если имя файла Sami совпадает с именем файла цифрового носителя (за исключением расширения имени файла).</span><span class="sxs-lookup"><span data-stu-id="11197-114">This association can occur when a SAMI file is specified by using the *sami* URL parameter, or automatically when the SAMI file has the same name as the digital media file (except for the file name extension).</span></span> <span data-ttu-id="11197-115">Если с текущим носителем не связан файл SAMI по умолчанию, это свойство получает строку нулевой длины ("").</span><span class="sxs-lookup"><span data-stu-id="11197-115">If there is no default SAMI file associated with the current media, this property gets a zero-length string ("").</span></span>

<span data-ttu-id="11197-116">Когда вы задаете значение с помощью **самифиленаме**, это значение сохраняется до тех пор, пока не будет задано новое значение (или до открытия нового элемента мультимедиа с помощью параметра URL-адреса SAMI).</span><span class="sxs-lookup"><span data-stu-id="11197-116">Once you set a value using **SAMIFileName**, that value persists until you set a new value (or until a new media item is opened using the sami URL parameter).</span></span> <span data-ttu-id="11197-117">Поэтому перед воспроизведением каждого нового элемента мультимедиа необходимо задать новое значение для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="11197-117">Therefore, you must set a new value for this property before you play each new media item.</span></span> <span data-ttu-id="11197-118">Таким образом, новое значение для **самифиленаме** вступит в силу при открытии следующего элемента мультимедиа (или при вызове **аксвиндовсмедиаплайер. Close** ).</span><span class="sxs-lookup"><span data-stu-id="11197-118">That way, the new value for **SAMIFileName** will take effect when the next media item is opened (or when **AxWindowsMediaPlayer.close** is called).</span></span> <span data-ttu-id="11197-119">Указание нового значения для **самифиленаме** не влияет на текущий носитель.</span><span class="sxs-lookup"><span data-stu-id="11197-119">Specifying a new value for **SAMIFileName** has no effect for the current media.</span></span>

<span data-ttu-id="11197-120">Чтобы проигрыватель Windows Media использовал файл SAMI по умолчанию, связанный с определенным элементом мультимедиа, перед воспроизведением следующего элемента мультимедиа задайте для **самифиленаме** строку нулевой длины ("").</span><span class="sxs-lookup"><span data-stu-id="11197-120">To cause Windows Media Player to use the default SAMI file associated with a particular media item, set **SAMIFileName** to a zero-length string ("") before you play the next media item.</span></span>

## <a name="requirements"></a><span data-ttu-id="11197-121">Требования</span><span class="sxs-lookup"><span data-stu-id="11197-121">Requirements</span></span>



| <span data-ttu-id="11197-122">Требование</span><span class="sxs-lookup"><span data-stu-id="11197-122">Requirement</span></span> | <span data-ttu-id="11197-123">Значение</span><span class="sxs-lookup"><span data-stu-id="11197-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11197-124">Версия</span><span class="sxs-lookup"><span data-stu-id="11197-124">Version</span></span><br/>   | <span data-ttu-id="11197-125">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="11197-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="11197-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="11197-126">Namespace</span></span><br/> | <span data-ttu-id="11197-127">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="11197-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="11197-128">Сборка</span><span class="sxs-lookup"><span data-stu-id="11197-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="11197-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="11197-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11197-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11197-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11197-131">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="11197-131">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="11197-132">**Аксвиндовсмедиаплайер. Close**</span><span class="sxs-lookup"><span data-stu-id="11197-132">**AxWindowsMediaPlayer.close**</span></span>](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[<span data-ttu-id="11197-133">**Интерфейс Ивмпклоседкаптион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="11197-133">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="11197-134">**Интерфейс IWMPClosedCaption2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="11197-134">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





