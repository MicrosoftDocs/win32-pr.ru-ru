---
description: Задает оптимальные параметры качества визуального элемента, используемые для кодировщика расширенного профиля Windows Media Video 9.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: Свойство MFPKEY_COMPRESSIONOPTIMIZATIONTYPE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3000caa10aa7db7d201cd11fd9a189fd6ac33591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692860"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a><span data-ttu-id="f26a5-103">МФПКЭЙ \_ компрессионоптимизатионтипе, свойство</span><span class="sxs-lookup"><span data-stu-id="f26a5-103">MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE Property</span></span>

<span data-ttu-id="f26a5-104">Задает оптимальные параметры качества визуального элемента, используемые для кодировщика расширенного профиля Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="f26a5-104">Specifies the optimal visual quality settings to use for the Windows Media Video 9 Advanced Profile encoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f26a5-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="f26a5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f26a5-106">g \_ всзвмвккомпрессионоптимизатионтипе</span><span class="sxs-lookup"><span data-stu-id="f26a5-106">g\_wszWMVCCompressionOptimizationType</span></span>

## <a name="data-type"></a><span data-ttu-id="f26a5-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f26a5-107">Data Type</span></span>

<span data-ttu-id="f26a5-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="f26a5-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="f26a5-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f26a5-109">Default Value</span></span>

<span data-ttu-id="f26a5-110">0</span><span class="sxs-lookup"><span data-stu-id="f26a5-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="f26a5-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f26a5-111">Remarks</span></span>

<span data-ttu-id="f26a5-112">Это свойство предоставляет быстрый способ настройки ряда параметров кодирования видео.</span><span class="sxs-lookup"><span data-stu-id="f26a5-112">This property provides a quick way to configure a number of video encoding options.</span></span> <span data-ttu-id="f26a5-113">Для него может быть задано одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f26a5-113">It may be set to one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f26a5-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f26a5-114">Value</span></span></th>
<th><span data-ttu-id="f26a5-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f26a5-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f26a5-116">0</span><span class="sxs-lookup"><span data-stu-id="f26a5-116">0</span></span></td>
<td><span data-ttu-id="f26a5-117">Кодек не будет выполнять принудительную оптимизацию и будет использовать все функции, заданные другими свойствами.</span><span class="sxs-lookup"><span data-stu-id="f26a5-117">The codec will not force optimization and will use whatever features are specified by other properties.</span></span> <span data-ttu-id="f26a5-118">Во многих случаях кодек будет использовать внутреннюю логику для определения параметров, если они не указаны.</span><span class="sxs-lookup"><span data-stu-id="f26a5-118">In many cases, the codec will use internal logic to determine settings if they are not specified.</span></span> <span data-ttu-id="f26a5-119">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f26a5-119">This is the default value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f26a5-120">1</span><span class="sxs-lookup"><span data-stu-id="f26a5-120">1</span></span></td>
<td><span data-ttu-id="f26a5-121">Включает функции, которые обеспечивают наилучшее качество визуального элемента. При использовании этого значения кодек настраивается так, как если бы были заданы следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="f26a5-121">Enables the features that will produce the best visual quality.Using this value configures the codec as if you had set the following properties:</span></span><br/>
<ul>
<li><span data-ttu-id="f26a5-122"><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</span><span class="sxs-lookup"><span data-stu-id="f26a5-122"><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</span></span></li>
<li><span data-ttu-id="f26a5-123"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</span><span class="sxs-lookup"><span data-stu-id="f26a5-123"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</span></span></li>
<li><span data-ttu-id="f26a5-124"><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</span><span class="sxs-lookup"><span data-stu-id="f26a5-124"><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</span></span></li>
<li><span data-ttu-id="f26a5-125"><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> =-1</span><span class="sxs-lookup"><span data-stu-id="f26a5-125"><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> = -1</span></span></li>
<li><span data-ttu-id="f26a5-126"><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</span><span class="sxs-lookup"><span data-stu-id="f26a5-126"><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</span></span></li>
<li><span data-ttu-id="f26a5-127"><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> =-1</span><span class="sxs-lookup"><span data-stu-id="f26a5-127"><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> = -1</span></span></li>
<li><span data-ttu-id="f26a5-128"><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</span><span class="sxs-lookup"><span data-stu-id="f26a5-128"><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</span></span></li>
</ul>
<span data-ttu-id="f26a5-129">Если задать любое из свойств в приведенном выше списке, заданное значение переопределит значения, связанные с этим параметром, за исключением <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span><span class="sxs-lookup"><span data-stu-id="f26a5-129">If you set any of the properties in the previous list, the value you set overrides the values associated with this setting, except for <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f26a5-130">Установка для свойства МФПКЭЙ компрессионоптимизатионтипе значения \_ 1 также влияет на установку параметра реестра дкуант в значение 2, а параметру реестра для метода стоимости вектора движения — значение 1.</span><span class="sxs-lookup"><span data-stu-id="f26a5-130">Setting the value of the MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE property to 1 also has the effect of setting the Dquant Option registry setting to 2, and the Motion Vector Cost Method registry setting to 1.</span></span> <span data-ttu-id="f26a5-131">Дополнительные сведения см. в веб-статье [Использование дополнительных параметров кодека расширенного профиля Windows Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).</span><span class="sxs-lookup"><span data-stu-id="f26a5-131">For more information, see the web article [Using the Advanced Settings of the Windows Media Video 9 Advanced Profile Codec](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).</span></span>

## <a name="requirements"></a><span data-ttu-id="f26a5-132">Требования</span><span class="sxs-lookup"><span data-stu-id="f26a5-132">Requirements</span></span>



| <span data-ttu-id="f26a5-133">Требование</span><span class="sxs-lookup"><span data-stu-id="f26a5-133">Requirement</span></span> | <span data-ttu-id="f26a5-134">Значение</span><span class="sxs-lookup"><span data-stu-id="f26a5-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f26a5-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f26a5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f26a5-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f26a5-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f26a5-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f26a5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f26a5-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f26a5-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f26a5-139">Header</span><span class="sxs-lookup"><span data-stu-id="f26a5-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="f26a5-140"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f26a5-140"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f26a5-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f26a5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f26a5-142">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f26a5-142">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




