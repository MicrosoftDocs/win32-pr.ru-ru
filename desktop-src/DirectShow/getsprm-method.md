---
description: Метод Жетспрм извлекает указанный регистр системного параметра.
ms.assetid: c6177f43-2809-4ef2-bc94-ac9a28f94621
title: Метод Жетспрм
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8b6898902eda55e0e877878343a25d82d03660
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103989909"
---
# <a name="getsprm-method"></a><span data-ttu-id="40c74-103">Метод Жетспрм</span><span class="sxs-lookup"><span data-stu-id="40c74-103">GetSPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="40c74-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="40c74-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="40c74-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="40c74-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="40c74-106">`GetSPRM`Метод извлекает указанный регистр системного параметра.</span><span class="sxs-lookup"><span data-stu-id="40c74-106">The `GetSPRM` method retrieves the specified system parameter register.</span></span>

``` syntax
[ iSPRM = ] MSWebDVD.GetSPRM(iIndex)
```

## <a name="parameters"></a><span data-ttu-id="40c74-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="40c74-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40c74-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*ииндекс*</span><span class="sxs-lookup"><span data-stu-id="40c74-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="40c74-109">Указывает регистр, значение которого необходимо получить в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="40c74-109">Specifies the register whose value you want to retrieve as an Integer.</span></span> <span data-ttu-id="40c74-110">Целое число должно находиться в диапазоне от 0 до 23.</span><span class="sxs-lookup"><span data-stu-id="40c74-110">The Integer must range from 0 through 23.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40c74-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="40c74-111">Return Value</span></span>

<span data-ttu-id="40c74-112">Возвращает целочисленное значение, представляющее содержимое указанного регистра.</span><span class="sxs-lookup"><span data-stu-id="40c74-112">Returns an integer value representing the contents of the specified register.</span></span>

## <a name="remarks"></a><span data-ttu-id="40c74-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40c74-113">Remarks</span></span>

<span data-ttu-id="40c74-114">Диск управляет регистрами системных параметров (Спрмс).</span><span class="sxs-lookup"><span data-stu-id="40c74-114">The disc controls system parameter registers (SPRMs).</span></span> <span data-ttu-id="40c74-115">Приложению проигрывателя не требуется доступ к этим регистрам для использования стандартных функций навигации.</span><span class="sxs-lookup"><span data-stu-id="40c74-115">A player application doesn't need to access these registers for any standard navigation functionality.</span></span> <span data-ttu-id="40c74-116">Спрмс представляет состояние проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="40c74-116">SPRMs represent the status of the player.</span></span> <span data-ttu-id="40c74-117">Каждый из них имеет смысл, задается пользовательскими предпочтениями, командами диска и другими случаями, когда приложение не имеет прямого контроля.</span><span class="sxs-lookup"><span data-stu-id="40c74-117">Each one has a meaning, set by user preferences, disc commands, and other occurrences that an application has no direct control over.</span></span> <span data-ttu-id="40c74-118">Приложение может считывать эти регистры, но не может выполнять запись в них.</span><span class="sxs-lookup"><span data-stu-id="40c74-118">An application can read these registers but cannot write to them.</span></span> <span data-ttu-id="40c74-119">Чтобы эффективно использовать эти регистры, вам, возможно, потребуется более подробная информация о командах перехода DVD, чем указано в этой документации.</span><span class="sxs-lookup"><span data-stu-id="40c74-119">To use these registers effectively, you will probably need a more detailed knowledge of the DVD navigation commands than is provided in this documentation.</span></span> <span data-ttu-id="40c74-120">В следующей таблице показано содержимое каждого регистра.</span><span class="sxs-lookup"><span data-stu-id="40c74-120">The following table shows the contents of each register.</span></span> <span data-ttu-id="40c74-121">Более подробные сведения о содержимом регистров см. в разделе [ **IDvdInfo2:: жеталлспрмс**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)</span><span class="sxs-lookup"><span data-stu-id="40c74-121">For more detailed information on the register contents, see [**IDvdInfo2::GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)</span></span>



| <span data-ttu-id="40c74-122">Регистрация</span><span class="sxs-lookup"><span data-stu-id="40c74-122">Register</span></span> | <span data-ttu-id="40c74-123">Содержимое</span><span class="sxs-lookup"><span data-stu-id="40c74-123">Contents</span></span>                        |
|----------|---------------------------------|
| <span data-ttu-id="40c74-124">0</span><span class="sxs-lookup"><span data-stu-id="40c74-124">0</span></span>        | <span data-ttu-id="40c74-125">Код языка меню</span><span class="sxs-lookup"><span data-stu-id="40c74-125">Menu language code</span></span>              |
| <span data-ttu-id="40c74-126">1</span><span class="sxs-lookup"><span data-stu-id="40c74-126">1</span></span>        | <span data-ttu-id="40c74-127">Номер аудиопотока</span><span class="sxs-lookup"><span data-stu-id="40c74-127">Audio stream number</span></span>             |
| <span data-ttu-id="40c74-128">2</span><span class="sxs-lookup"><span data-stu-id="40c74-128">2</span></span>        | <span data-ttu-id="40c74-129">Номер потока субтитров</span><span class="sxs-lookup"><span data-stu-id="40c74-129">Subpicture stream number</span></span>        |
| <span data-ttu-id="40c74-130">3</span><span class="sxs-lookup"><span data-stu-id="40c74-130">3</span></span>        | <span data-ttu-id="40c74-131">Текущий номер угла</span><span class="sxs-lookup"><span data-stu-id="40c74-131">Current angle number</span></span>            |
| <span data-ttu-id="40c74-132">4</span><span class="sxs-lookup"><span data-stu-id="40c74-132">4</span></span>        | <span data-ttu-id="40c74-133">Номер текущего заголовка</span><span class="sxs-lookup"><span data-stu-id="40c74-133">Current title number</span></span>            |
| <span data-ttu-id="40c74-134">5</span><span class="sxs-lookup"><span data-stu-id="40c74-134">5</span></span>        | <span data-ttu-id="40c74-135">Номер заголовка</span><span class="sxs-lookup"><span data-stu-id="40c74-135">Title number</span></span>                    |
| <span data-ttu-id="40c74-136">6</span><span class="sxs-lookup"><span data-stu-id="40c74-136">6</span></span>        | <span data-ttu-id="40c74-137">Номер PGC</span><span class="sxs-lookup"><span data-stu-id="40c74-137">PGC number</span></span>                      |
| <span data-ttu-id="40c74-138">7</span><span class="sxs-lookup"><span data-stu-id="40c74-138">7</span></span>        | <span data-ttu-id="40c74-139">Текущий номер главы (PTT)</span><span class="sxs-lookup"><span data-stu-id="40c74-139">Current chapter number (PTT)</span></span>    |
| <span data-ttu-id="40c74-140">8</span><span class="sxs-lookup"><span data-stu-id="40c74-140">8</span></span>        | <span data-ttu-id="40c74-141">Номер выделенной кнопки</span><span class="sxs-lookup"><span data-stu-id="40c74-141">Highlighted button number</span></span>       |
| <span data-ttu-id="40c74-142">9</span><span class="sxs-lookup"><span data-stu-id="40c74-142">9</span></span>        | <span data-ttu-id="40c74-143">Таймер навигации</span><span class="sxs-lookup"><span data-stu-id="40c74-143">Navigation timer</span></span>                |
| <span data-ttu-id="40c74-144">10</span><span class="sxs-lookup"><span data-stu-id="40c74-144">10</span></span>       | <span data-ttu-id="40c74-145">Переход PGC для навигации.</span><span class="sxs-lookup"><span data-stu-id="40c74-145">PGC jump for nav.</span></span> <span data-ttu-id="40c74-146">Таймер</span><span class="sxs-lookup"><span data-stu-id="40c74-146">timer</span></span>         |
| <span data-ttu-id="40c74-147">11</span><span class="sxs-lookup"><span data-stu-id="40c74-147">11</span></span>       | <span data-ttu-id="40c74-148">Режим звуковой презентации Караоке</span><span class="sxs-lookup"><span data-stu-id="40c74-148">Karaoke audio presentation mode</span></span> |
| <span data-ttu-id="40c74-149">12</span><span class="sxs-lookup"><span data-stu-id="40c74-149">12</span></span>       | <span data-ttu-id="40c74-150">Код страны или региона ПМЛ</span><span class="sxs-lookup"><span data-stu-id="40c74-150">PML country/region code</span></span>         |
| <span data-ttu-id="40c74-151">13</span><span class="sxs-lookup"><span data-stu-id="40c74-151">13</span></span>       | <span data-ttu-id="40c74-152">пмл</span><span class="sxs-lookup"><span data-stu-id="40c74-152">PML</span></span>                             |
| <span data-ttu-id="40c74-153">14</span><span class="sxs-lookup"><span data-stu-id="40c74-153">14</span></span>       | <span data-ttu-id="40c74-154">Параметр видео</span><span class="sxs-lookup"><span data-stu-id="40c74-154">Video setting</span></span>                   |
| <span data-ttu-id="40c74-155">15</span><span class="sxs-lookup"><span data-stu-id="40c74-155">15</span></span>       | <span data-ttu-id="40c74-156">Звуковые возможности</span><span class="sxs-lookup"><span data-stu-id="40c74-156">Audio capability</span></span>                |
| <span data-ttu-id="40c74-157">16</span><span class="sxs-lookup"><span data-stu-id="40c74-157">16</span></span>       | <span data-ttu-id="40c74-158">Язык звука</span><span class="sxs-lookup"><span data-stu-id="40c74-158">Audio language</span></span>                  |
| <span data-ttu-id="40c74-159">17</span><span class="sxs-lookup"><span data-stu-id="40c74-159">17</span></span>       | <span data-ttu-id="40c74-160">Расширение языка звука</span><span class="sxs-lookup"><span data-stu-id="40c74-160">Audio language extension</span></span>        |
| <span data-ttu-id="40c74-161">18</span><span class="sxs-lookup"><span data-stu-id="40c74-161">18</span></span>       | <span data-ttu-id="40c74-162">Язык субтитров</span><span class="sxs-lookup"><span data-stu-id="40c74-162">Subpicture language</span></span>             |
| <span data-ttu-id="40c74-163">19</span><span class="sxs-lookup"><span data-stu-id="40c74-163">19</span></span>       | <span data-ttu-id="40c74-164">Расширение языка субтитров</span><span class="sxs-lookup"><span data-stu-id="40c74-164">Subpicture language extension</span></span>   |
| <span data-ttu-id="40c74-165">20</span><span class="sxs-lookup"><span data-stu-id="40c74-165">20</span></span>       | <span data-ttu-id="40c74-166">Код региона проигрывателя</span><span class="sxs-lookup"><span data-stu-id="40c74-166">Player region code</span></span>              |
| <span data-ttu-id="40c74-167">21</span><span class="sxs-lookup"><span data-stu-id="40c74-167">21</span></span>       | <span data-ttu-id="40c74-168">Зарезервировано</span><span class="sxs-lookup"><span data-stu-id="40c74-168">Reserved</span></span>                        |
| <span data-ttu-id="40c74-169">22</span><span class="sxs-lookup"><span data-stu-id="40c74-169">22</span></span>       | <span data-ttu-id="40c74-170">Зарезервировано</span><span class="sxs-lookup"><span data-stu-id="40c74-170">Reserved</span></span>                        |
| <span data-ttu-id="40c74-171">23</span><span class="sxs-lookup"><span data-stu-id="40c74-171">23</span></span>       | <span data-ttu-id="40c74-172">Зарезервировано</span><span class="sxs-lookup"><span data-stu-id="40c74-172">Reserved</span></span>                        |



 

## <a name="see-also"></a><span data-ttu-id="40c74-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40c74-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40c74-174">**жетгпрм**</span><span class="sxs-lookup"><span data-stu-id="40c74-174">**GetGPRM**</span></span>](getgprm-method.md)
</dt> <dt>

[<span data-ttu-id="40c74-175">**сетгпрм**</span><span class="sxs-lookup"><span data-stu-id="40c74-175">**SetGPRM**</span></span>](setgprm-method.md)
</dt> </dl>

 

 



