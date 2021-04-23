---
description: Свойство Property объекта Суммаринфо задает или получает значение для указанного свойства в информационном потоке сводки.
ms.assetid: 8e8f0987-c92b-43f3-a61a-35099188c629
title: Суммаринфо. Property, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e51773a930b8868e31a7e88848300a62b717912
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675359"
---
# <a name="summaryinfoproperty-property"></a><span data-ttu-id="33697-103">Суммаринфо. Property, свойство</span><span class="sxs-lookup"><span data-stu-id="33697-103">SummaryInfo.Property property</span></span>

<span data-ttu-id="33697-104">Свойство **Property** объекта [**суммаринфо**](summaryinfo-object.md) задает или получает значение для указанного свойства в информационном потоке сводки.</span><span class="sxs-lookup"><span data-stu-id="33697-104">The **Property** property of the [**SummaryInfo**](summaryinfo-object.md) object sets or gets the value for the specified property in the summary information stream.</span></span> <span data-ttu-id="33697-105">Свойства считываются при создании объекта [**суммаринфо**](summaryinfo-object.md) , но не записываются, пока не будет вызван метод [**PERSISTED**](summaryinfo-persist.md) .</span><span class="sxs-lookup"><span data-stu-id="33697-105">The properties are read when the [**SummaryInfo**](summaryinfo-object.md) object is created, but they are not written until the [**Persist**](summaryinfo-persist.md) method is called.</span></span> <span data-ttu-id="33697-106">Установка свойства в значение Empty приводит к его удалению; Аналогично, при запросе несуществующего свойства возвращается пустое значение.</span><span class="sxs-lookup"><span data-stu-id="33697-106">Setting a property to Empty causes its removal; likewise, requesting a nonexistent property returns an Empty value.</span></span> <span data-ttu-id="33697-107">В противном случае значения могут передаваться как строки, целые числа или типы даты и времени.</span><span class="sxs-lookup"><span data-stu-id="33697-107">Otherwise values may be transferred as strings, integers, or date (date time) types.</span></span>

<span data-ttu-id="33697-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="33697-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="33697-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33697-109">Syntax</span></span>


```JScript
propVal = SummaryInfo.Property
```



## <a name="property-value"></a><span data-ttu-id="33697-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="33697-110">Property value</span></span>

<span data-ttu-id="33697-111">Обязательный идентификатор свойства одного из свойств сводки.</span><span class="sxs-lookup"><span data-stu-id="33697-111">Required property ID of one of the summary properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="33697-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33697-112">Remarks</span></span>

<span data-ttu-id="33697-113">**Стандартные идентификаторы свойств сводки**</span><span class="sxs-lookup"><span data-stu-id="33697-113">**Standard Summary Property IDs**</span></span>

<span data-ttu-id="33697-114">(не перечисление)</span><span class="sxs-lookup"><span data-stu-id="33697-114">(not an enumeration)</span></span>



| <span data-ttu-id="33697-115">Имя параметра</span><span class="sxs-lookup"><span data-stu-id="33697-115">Parameter name</span></span>     | <span data-ttu-id="33697-116">Значение</span><span class="sxs-lookup"><span data-stu-id="33697-116">Value</span></span> | <span data-ttu-id="33697-117">Описание</span><span class="sxs-lookup"><span data-stu-id="33697-117">Description</span></span>                                       |
|--------------------|-------|---------------------------------------------------|
| <span data-ttu-id="33697-118">\_словарь PID</span><span class="sxs-lookup"><span data-stu-id="33697-118">PID\_DICTIONARY</span></span>    | <span data-ttu-id="33697-119">0</span><span class="sxs-lookup"><span data-stu-id="33697-119">0</span></span>     | <span data-ttu-id="33697-120">Специальный формат, не поддерживаемый объектом Суммаринфо</span><span class="sxs-lookup"><span data-stu-id="33697-120">Special format, not support by SummaryInfo object</span></span> |
| <span data-ttu-id="33697-121">\_кодовая страница PID</span><span class="sxs-lookup"><span data-stu-id="33697-121">PID\_CODEPAGE</span></span>      | <span data-ttu-id="33697-122">1</span><span class="sxs-lookup"><span data-stu-id="33697-122">1</span></span>     | <span data-ttu-id="33697-123">VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="33697-123">VT\_I2</span></span>                                            |
| <span data-ttu-id="33697-124">\_название PID</span><span class="sxs-lookup"><span data-stu-id="33697-124">PID\_TITLE</span></span>         | <span data-ttu-id="33697-125">2</span><span class="sxs-lookup"><span data-stu-id="33697-125">2</span></span>     | <span data-ttu-id="33697-126">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="33697-126">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="33697-127">\_Тема PID</span><span class="sxs-lookup"><span data-stu-id="33697-127">PID\_SUBJECT</span></span>       | <span data-ttu-id="33697-128">3</span><span class="sxs-lookup"><span data-stu-id="33697-128">3</span></span>     | <span data-ttu-id="33697-129">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="33697-129">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="33697-130">\_Автор PID</span><span class="sxs-lookup"><span data-stu-id="33697-130">PID\_AUTHOR</span></span>        | <span data-ttu-id="33697-131">4</span><span class="sxs-lookup"><span data-stu-id="33697-131">4</span></span>     | <span data-ttu-id="33697-132">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="33697-132">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="33697-133">\_Ключевые слова PID</span><span class="sxs-lookup"><span data-stu-id="33697-133">PID\_KEYWORDS</span></span>      | <span data-ttu-id="33697-134">5</span><span class="sxs-lookup"><span data-stu-id="33697-134">5</span></span>     | <span data-ttu-id="33697-135">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="33697-135">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="33697-136">\_Комментарии PID</span><span class="sxs-lookup"><span data-stu-id="33697-136">PID\_COMMENTS</span></span>      | <span data-ttu-id="33697-137">6</span><span class="sxs-lookup"><span data-stu-id="33697-137">6</span></span>     | <span data-ttu-id="33697-138">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="33697-138">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="33697-139">\_шаблон PID</span><span class="sxs-lookup"><span data-stu-id="33697-139">PID\_TEMPLATE</span></span>      | <span data-ttu-id="33697-140">7</span><span class="sxs-lookup"><span data-stu-id="33697-140">7</span></span>     | <span data-ttu-id="33697-141">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="33697-141">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="33697-142">Идентификатор процесса \_ ластаусор</span><span class="sxs-lookup"><span data-stu-id="33697-142">PID\_LASTAUTHOR</span></span>    | <span data-ttu-id="33697-143">8</span><span class="sxs-lookup"><span data-stu-id="33697-143">8</span></span>     | <span data-ttu-id="33697-144">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="33697-144">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="33697-145">Идентификатор процесса \_ ревнумбер</span><span class="sxs-lookup"><span data-stu-id="33697-145">PID\_REVNUMBER</span></span>     | <span data-ttu-id="33697-146">9</span><span class="sxs-lookup"><span data-stu-id="33697-146">9</span></span>     | <span data-ttu-id="33697-147">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="33697-147">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="33697-148">Идентификатор процесса \_ едиттиме</span><span class="sxs-lookup"><span data-stu-id="33697-148">PID\_EDITTIME</span></span>      | <span data-ttu-id="33697-149">10</span><span class="sxs-lookup"><span data-stu-id="33697-149">10</span></span>    | <span data-ttu-id="33697-150">VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="33697-150">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="33697-151">Идентификатор процесса \_ ластпринтед</span><span class="sxs-lookup"><span data-stu-id="33697-151">PID\_LASTPRINTED</span></span>   | <span data-ttu-id="33697-152">11</span><span class="sxs-lookup"><span data-stu-id="33697-152">11</span></span>    | <span data-ttu-id="33697-153">VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="33697-153">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="33697-154">PID \_ Create \_ DTM</span><span class="sxs-lookup"><span data-stu-id="33697-154">PID\_CREATE\_DTM</span></span>   | <span data-ttu-id="33697-155">12</span><span class="sxs-lookup"><span data-stu-id="33697-155">12</span></span>    | <span data-ttu-id="33697-156">VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="33697-156">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="33697-157">PID \_ ластсаве \_ DTM</span><span class="sxs-lookup"><span data-stu-id="33697-157">PID\_LASTSAVE\_DTM</span></span> | <span data-ttu-id="33697-158">13</span><span class="sxs-lookup"><span data-stu-id="33697-158">13</span></span>    | <span data-ttu-id="33697-159">VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="33697-159">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="33697-160">Идентификатор процесса \_ PAGECOUNT</span><span class="sxs-lookup"><span data-stu-id="33697-160">PID\_PAGECOUNT</span></span>     | <span data-ttu-id="33697-161">14</span><span class="sxs-lookup"><span data-stu-id="33697-161">14</span></span>    | <span data-ttu-id="33697-162">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="33697-162">VT\_I4</span></span>                                            |
| <span data-ttu-id="33697-163">номер процесса \_ WORDCOUNT</span><span class="sxs-lookup"><span data-stu-id="33697-163">PID\_WORDCOUNT</span></span>     | <span data-ttu-id="33697-164">15</span><span class="sxs-lookup"><span data-stu-id="33697-164">15</span></span>    | <span data-ttu-id="33697-165">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="33697-165">VT\_I4</span></span>                                            |
| <span data-ttu-id="33697-166">Идентификатор идентификатора \_ CHARCOUNT</span><span class="sxs-lookup"><span data-stu-id="33697-166">PID\_CHARCOUNT</span></span>     | <span data-ttu-id="33697-167">16</span><span class="sxs-lookup"><span data-stu-id="33697-167">16</span></span>    | <span data-ttu-id="33697-168">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="33697-168">VT\_I4</span></span>                                            |
| <span data-ttu-id="33697-169">\_эскиз PID</span><span class="sxs-lookup"><span data-stu-id="33697-169">PID\_THUMBNAIL</span></span>     | <span data-ttu-id="33697-170">17</span><span class="sxs-lookup"><span data-stu-id="33697-170">17</span></span>    | <span data-ttu-id="33697-171">VT \_ CF (не поддерживается)</span><span class="sxs-lookup"><span data-stu-id="33697-171">VT\_CF (not supported)</span></span>                            |
| <span data-ttu-id="33697-172">PID \_ APPNAME</span><span class="sxs-lookup"><span data-stu-id="33697-172">PID\_APPNAME</span></span>       | <span data-ttu-id="33697-173">18</span><span class="sxs-lookup"><span data-stu-id="33697-173">18</span></span>    | <span data-ttu-id="33697-174">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="33697-174">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="33697-175">\_Безопасность PID</span><span class="sxs-lookup"><span data-stu-id="33697-175">PID\_SECURITY</span></span>      | <span data-ttu-id="33697-176">19</span><span class="sxs-lookup"><span data-stu-id="33697-176">19</span></span>    | <span data-ttu-id="33697-177">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="33697-177">VT\_I4</span></span>                                            |



 

<span data-ttu-id="33697-178">**Типы данных свойств**</span><span class="sxs-lookup"><span data-stu-id="33697-178">**Property Data Types**</span></span>

<span data-ttu-id="33697-179">(не перечисление)</span><span class="sxs-lookup"><span data-stu-id="33697-179">(not an enumeration)</span></span>



| <span data-ttu-id="33697-180">Имя параметра</span><span class="sxs-lookup"><span data-stu-id="33697-180">Parameter name</span></span> | <span data-ttu-id="33697-181">Значение</span><span class="sxs-lookup"><span data-stu-id="33697-181">Value</span></span> | <span data-ttu-id="33697-182">Описание</span><span class="sxs-lookup"><span data-stu-id="33697-182">Description</span></span>                                                                              |
|----------------|-------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="33697-183">VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="33697-183">VT\_I2</span></span>         | <span data-ttu-id="33697-184">2</span><span class="sxs-lookup"><span data-stu-id="33697-184">2</span></span>     | <span data-ttu-id="33697-185">16-разрядное целое число</span><span class="sxs-lookup"><span data-stu-id="33697-185">16-bit integer</span></span>                                                                           |
| <span data-ttu-id="33697-186">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="33697-186">VT\_I4</span></span>         | <span data-ttu-id="33697-187">3</span><span class="sxs-lookup"><span data-stu-id="33697-187">3</span></span>     | <span data-ttu-id="33697-188">32-разрядное целое число</span><span class="sxs-lookup"><span data-stu-id="33697-188">32-bit integer</span></span>                                                                           |
| <span data-ttu-id="33697-189">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="33697-189">VT\_LPSTR</span></span>      | <span data-ttu-id="33697-190">30</span><span class="sxs-lookup"><span data-stu-id="33697-190">30</span></span>    | <span data-ttu-id="33697-191">Строка</span><span class="sxs-lookup"><span data-stu-id="33697-191">String</span></span>                                                                                   |
| <span data-ttu-id="33697-192">VT \_ fileTime</span><span class="sxs-lookup"><span data-stu-id="33697-192">VT\_FILETIME</span></span>   | <span data-ttu-id="33697-193">64</span><span class="sxs-lookup"><span data-stu-id="33697-193">64</span></span>    | <span data-ttu-id="33697-194">Дата и время (FILETIME, преобразованные в вариантное время)</span><span class="sxs-lookup"><span data-stu-id="33697-194">Date time (FILETIME, converted to Variant time)</span></span>                                          |
| <span data-ttu-id="33697-195">VT \_ CF</span><span class="sxs-lookup"><span data-stu-id="33697-195">VT\_CF</span></span>         | <span data-ttu-id="33697-196">71</span><span class="sxs-lookup"><span data-stu-id="33697-196">71</span></span>    | <span data-ttu-id="33697-197">Формат буфера обмена + данные, не обрабатываемые объектом [**суммаринфо**](summaryinfo-object.md)</span><span class="sxs-lookup"><span data-stu-id="33697-197">Clipboard format + data, not handled by [**SummaryInfo**](summaryinfo-object.md) object</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="33697-198">Требования</span><span class="sxs-lookup"><span data-stu-id="33697-198">Requirements</span></span>



| <span data-ttu-id="33697-199">Требование</span><span class="sxs-lookup"><span data-stu-id="33697-199">Requirement</span></span> | <span data-ttu-id="33697-200">Значение</span><span class="sxs-lookup"><span data-stu-id="33697-200">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33697-201">Версия</span><span class="sxs-lookup"><span data-stu-id="33697-201">Version</span></span><br/> | <span data-ttu-id="33697-202">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="33697-202">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="33697-203">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="33697-203">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="33697-204">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="33697-204">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="33697-205">DLL</span><span class="sxs-lookup"><span data-stu-id="33697-205">DLL</span></span><br/>     | <dl> <span data-ttu-id="33697-206"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33697-206"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="33697-207">IID</span><span class="sxs-lookup"><span data-stu-id="33697-207">IID</span></span><br/>     | <span data-ttu-id="33697-208">IID \_ исуммаринфо определяется как 000C109B-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="33697-208">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="33697-209">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33697-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33697-210">**мсисуммаринфосетпроперти**</span><span class="sxs-lookup"><span data-stu-id="33697-210">**MsiSummaryInfoSetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)
</dt> <dt>

[<span data-ttu-id="33697-211">**мсисуммаринфожетпроперти**</span><span class="sxs-lookup"><span data-stu-id="33697-211">**MsiSummaryInfoGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)
</dt> </dl>

 

 




