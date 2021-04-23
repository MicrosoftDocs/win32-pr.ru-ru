---
description: Коды возврата WMI, указывающие состояние и не указывающие на ошибку.
ms.assetid: 36faa3fb-9496-47ca-bdba-f8eb52a06ff7
ms.tgt_platform: multiple
title: Константы WMI, отличные от ошибок (Вбемкли. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0880c9fda00f03c1fa8b174242bfc84ed9d75ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263924"
---
# <a name="wmi-non-error-constants"></a><span data-ttu-id="28392-103">Константы WMI, отличные от ошибок</span><span class="sxs-lookup"><span data-stu-id="28392-103">WMI Non-Error Constants</span></span>

<span data-ttu-id="28392-104">Коды возврата WMI, указывающие состояние и не указывающие на ошибку.</span><span class="sxs-lookup"><span data-stu-id="28392-104">WMI return codes that indicate status and do not indicate an error.</span></span>

<span data-ttu-id="28392-105">Если операция не приводит к ошибке, WMI возвращает один из следующих кодов как **HRESULT** , указывающий состояние операции.</span><span class="sxs-lookup"><span data-stu-id="28392-105">If an operation does not result in an error, WMI returns one of the following codes as an **HRESULT** that indicates the status of the operation.</span></span>

> [!Note]  
> <span data-ttu-id="28392-106">Некоторые методы в классах WMI могут возвращать системные и сетевые коды ошибок (например, 64).</span><span class="sxs-lookup"><span data-stu-id="28392-106">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="28392-107">Определение этих типов кодов ошибок можно проверить с помощью команды **net helpmsg** в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="28392-107">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="28392-108">Например, команда **net helpmsg 64** возвращает сообщение: указанное сетевое имя больше недоступно.</span><span class="sxs-lookup"><span data-stu-id="28392-108">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

 

<span data-ttu-id="28392-109">В C++ можно вызвать [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) и указать **C: \\ Windows \\ system32 \\ WBEM \\wmiutils.dll** в качестве модуля сообщения.</span><span class="sxs-lookup"><span data-stu-id="28392-109">In C++, you can call [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) and specify **C:\\Windows\\System32\\wbem\\wmiutils.dll** as the message module.</span></span>

<dl> <dt>

<span data-ttu-id="28392-110"><span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**WBEM \_ \_ без \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="28392-110"><span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**WBEM\_S\_NO\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28392-111">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="28392-111">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="28392-112">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="28392-112">The operation was successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28392-113"><span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM \_ , \_ ложь**</span><span class="sxs-lookup"><span data-stu-id="28392-113"><span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM\_S\_FALSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28392-114">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="28392-114">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="28392-115">Больше нет доступных объектов, число возвращаемых объектов меньше запрошенного числа или это конец перечисления.</span><span class="sxs-lookup"><span data-stu-id="28392-115">No more objects are available, the number of objects returned is less than the number requested, or this is the end of an enumeration.</span></span> <span data-ttu-id="28392-116">Это значение также возвращается при вызове этого метода со значением 0 для параметра *укаунт* .</span><span class="sxs-lookup"><span data-stu-id="28392-116">This value is also returned when this method is called with a value of 0 for the *uCount* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28392-117"><span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM \_ \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="28392-117"><span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM\_S\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28392-118">262145 (0x40001)</span><span class="sxs-lookup"><span data-stu-id="28392-118">262145 (0x40001)</span></span>
</dt> <dt>



<span data-ttu-id="28392-119">Предпринята попытка создать уже существующий объект или класс.</span><span class="sxs-lookup"><span data-stu-id="28392-119">An attempt was made to create an object or class that already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28392-120"><span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**\_Установка WBEM \_ \_ \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="28392-120"><span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**WBEM\_S\_RESET\_TO\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28392-121">262146 (0x40002)</span><span class="sxs-lookup"><span data-stu-id="28392-121">262146 (0x40002)</span></span>
</dt> <dt>



<span data-ttu-id="28392-122">Удалено переопределенное свойство.</span><span class="sxs-lookup"><span data-stu-id="28392-122">An overridden property was deleted.</span></span> <span data-ttu-id="28392-123">Это значение возвращается, чтобы сообщить, что исходное переопределенное значение было восстановлено в результате удаления.</span><span class="sxs-lookup"><span data-stu-id="28392-123">This value is returned to signal that the original non-overridden value has been restored as a result of the deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28392-124"><span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**\_другой WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="28392-124"><span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM\_S\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28392-125">262147 (0x40003)</span><span class="sxs-lookup"><span data-stu-id="28392-125">262147 (0x40003)</span></span>
</dt> <dt>



<span data-ttu-id="28392-126">Элементы (объекты, классы и т. д.), которые сравниваются, не идентичны.</span><span class="sxs-lookup"><span data-stu-id="28392-126">The items (objects, classes, and so on) that are being compared are not identical.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28392-127"><span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**WBEM \_ , \_ TIMEDOUT**</span><span class="sxs-lookup"><span data-stu-id="28392-127"><span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**WBEM\_S\_TIMEDOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28392-128">262148 (0x40004)</span><span class="sxs-lookup"><span data-stu-id="28392-128">262148 (0x40004)</span></span>
</dt> <dt>



<span data-ttu-id="28392-129">Время ожидания вызова истекло. Это не условие ошибки.</span><span class="sxs-lookup"><span data-stu-id="28392-129">A call timed out. This is not an error condition.</span></span> <span data-ttu-id="28392-130">Поэтому могут также возвращаться некоторые результаты.</span><span class="sxs-lookup"><span data-stu-id="28392-130">Therefore, some results may have also been returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28392-131"><span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM, больше \_ \_ нет \_ \_ данных**</span><span class="sxs-lookup"><span data-stu-id="28392-131"><span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM\_S\_NO\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28392-132">262149 (0x40005)</span><span class="sxs-lookup"><span data-stu-id="28392-132">262149 (0x40005)</span></span>
</dt> <dt>



<span data-ttu-id="28392-133">В перечислении больше нет доступных данных, и пользователь должен завершить перечисление.</span><span class="sxs-lookup"><span data-stu-id="28392-133">No more data is available from the enumeration, and the user must terminate the enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28392-134"><span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**\_Операция WBEM \_ S \_ отменена**</span><span class="sxs-lookup"><span data-stu-id="28392-134"><span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**WBEM\_S\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28392-135">262150 (0x40006)</span><span class="sxs-lookup"><span data-stu-id="28392-135">262150 (0x40006)</span></span>
</dt> <dt>



<span data-ttu-id="28392-136">Операция была намеренно или непреднамеренно отменена.</span><span class="sxs-lookup"><span data-stu-id="28392-136">The operation was intentionally or unintentionally canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28392-137"><span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**\_ \_ Ожидание с WBEM**</span><span class="sxs-lookup"><span data-stu-id="28392-137"><span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM\_S\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28392-138">262151 (0x40007)</span><span class="sxs-lookup"><span data-stu-id="28392-138">262151 (0x40007)</span></span>
</dt> <dt>



<span data-ttu-id="28392-139">Запрос все еще выполняется, и результаты еще не доступны.</span><span class="sxs-lookup"><span data-stu-id="28392-139">A request is still in progress, and the results are not yet available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28392-140"><span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**\_объекты с \_ ПОВТОРЯЮЩИМИСЯ \_ объектами WBEM**</span><span class="sxs-lookup"><span data-stu-id="28392-140"><span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**WBEM\_S\_DUPLICATE\_OBJECTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28392-141">262152 (0x40008)</span><span class="sxs-lookup"><span data-stu-id="28392-141">262152 (0x40008)</span></span>
</dt> <dt>



<span data-ttu-id="28392-142">В результирующем наборе перечисления обнаружено несколько копий одного объекта.</span><span class="sxs-lookup"><span data-stu-id="28392-142">More than one copy of the same object was detected in the result set of an enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28392-143"><span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**\_ \_ доступ к WBEM S \_ запрещен**</span><span class="sxs-lookup"><span data-stu-id="28392-143"><span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**WBEM\_S\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28392-144">262153 (0x40009)</span><span class="sxs-lookup"><span data-stu-id="28392-144">262153 (0x40009)</span></span>
</dt> <dt>



<span data-ttu-id="28392-145">Пользователю отказано в доступе к некоторым, но не ко всем ресурсам.</span><span class="sxs-lookup"><span data-stu-id="28392-145">The user was denied access to some but not all resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28392-146"><span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**\_неполные \_ \_ результаты с WBEM**</span><span class="sxs-lookup"><span data-stu-id="28392-146"><span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**WBEM\_S\_PARTIAL\_RESULTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28392-147">262160 (0x40010)</span><span class="sxs-lookup"><span data-stu-id="28392-147">262160 (0x40010)</span></span>
</dt> <dt>



<span data-ttu-id="28392-148">Пользователь не получил все запрошенные объекты из-за недоступных ресурсов (кроме нарушений безопасности).</span><span class="sxs-lookup"><span data-stu-id="28392-148">The user did not receive all of the objects requested due to inaccessible resources (other than security violations).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28392-149"><span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**\_ \_ ограниченная \_ Служба WBEM**</span><span class="sxs-lookup"><span data-stu-id="28392-149"><span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**WBEM\_S\_LIMITED\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28392-150">274433 (0x43001)</span><span class="sxs-lookup"><span data-stu-id="28392-150">274433 (0x43001)</span></span>
</dt> <dt>



<span data-ttu-id="28392-151">Поставщик может иметь ограниченную службу.</span><span class="sxs-lookup"><span data-stu-id="28392-151">The provider is capable of limited service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="28392-152"><span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**\_ \_ непрямое \_ Обновление WBEM**</span><span class="sxs-lookup"><span data-stu-id="28392-152"><span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**WBEM\_S\_INDIRECTLY\_UPDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28392-153">274434 (0x43002)</span><span class="sxs-lookup"><span data-stu-id="28392-153">274434 (0x43002)</span></span>
</dt> <dt>



<span data-ttu-id="28392-154">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="28392-154">Reserved for future use.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="28392-155">Требования</span><span class="sxs-lookup"><span data-stu-id="28392-155">Requirements</span></span>



| <span data-ttu-id="28392-156">Требование</span><span class="sxs-lookup"><span data-stu-id="28392-156">Requirement</span></span> | <span data-ttu-id="28392-157">Значение</span><span class="sxs-lookup"><span data-stu-id="28392-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28392-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28392-158">Minimum supported client</span></span><br/> | <span data-ttu-id="28392-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28392-159">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="28392-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28392-160">Minimum supported server</span></span><br/> | <span data-ttu-id="28392-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28392-161">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="28392-162">Header</span><span class="sxs-lookup"><span data-stu-id="28392-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="28392-163"><dt>Вбемкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="28392-163"><dt>WbemCli.h</dt></span></span> </dl>   |
| <span data-ttu-id="28392-164">IDL</span><span class="sxs-lookup"><span data-stu-id="28392-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="28392-165"><dt>Вбемкли. idl</dt></span><span class="sxs-lookup"><span data-stu-id="28392-165"><dt>WbemCli.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28392-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28392-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28392-167">Коды возврата WMI</span><span class="sxs-lookup"><span data-stu-id="28392-167">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

