---
description: Задает первый байт параметра (P1) для единицы данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: 359df5cc-10a7-4093-9a77-f3eb0b98545a
title: 'Искардкмд: метод ut_P1:p (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 18f7563fd6ae1c3490e36896b22af3a6034168e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647483"
---
# <a name="iscardcmdput_p1-method"></a><span data-ttu-id="9b7b2-103">Искардкмд: метод:p UT \_ P1</span><span class="sxs-lookup"><span data-stu-id="9b7b2-103">ISCardCmd::put\_P1 method</span></span>

<span data-ttu-id="9b7b2-104">\[Метод **размещения \_ P1** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-104">\[The **put\_P1** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9b7b2-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9b7b2-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="9b7b2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9b7b2-107">Метод **размещения \_ P1** задает первый байт параметра (P1) для [*единицы данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="9b7b2-107">The **put\_P1** method sets the first parameter (P1) byte of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="9b7b2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b7b2-108">Syntax</span></span>


```C++
HRESULT put_P1(
  [in] BYTE byP1
);
```



## <a name="parameters"></a><span data-ttu-id="9b7b2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b7b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b7b2-110">*byP1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b7b2-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b7b2-111">Байт, который является полем P1.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-111">The byte that is the P1 field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b7b2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b7b2-112">Return value</span></span>

<span data-ttu-id="9b7b2-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="9b7b2-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9b7b2-114">Return code</span></span>                                                                                   | <span data-ttu-id="9b7b2-115">Описание</span><span class="sxs-lookup"><span data-stu-id="9b7b2-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="9b7b2-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9b7b2-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9b7b2-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="9b7b2-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="9b7b2-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9b7b2-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9b7b2-119">Недопустимый параметр *byP1* .</span><span class="sxs-lookup"><span data-stu-id="9b7b2-119">The *byP1* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="9b7b2-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9b7b2-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9b7b2-121">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="9b7b2-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b7b2-122">Remarks</span></span>

<span data-ttu-id="9b7b2-123">Чтобы задать значение P2 объекта КАТЕГОРИЯХ APDU, вызовите [**Get \_ P2**](iscardcmd-get-p2.md).</span><span class="sxs-lookup"><span data-stu-id="9b7b2-123">To set the P2 value of the APDU, call [**get\_P2**](iscardcmd-get-p2.md).</span></span>

<span data-ttu-id="9b7b2-124">Чтобы получить существующие значения P1, P2 и P3, вызовите [**Get \_ P1**](iscardcmd-get-p1.md), [**Get \_ P2**](iscardcmd-get-p2.md) или [**Get \_ P3**](iscardcmd-get-p3.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-124">To retrieve the existing P1, P2, and P3 values, call [**get\_P1**](iscardcmd-get-p1.md), [**get\_P2**](iscardcmd-get-p2.md) or [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="9b7b2-125">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="9b7b2-125">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="9b7b2-126">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="9b7b2-127">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9b7b2-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9b7b2-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="9b7b2-128">Examples</span></span>

<span data-ttu-id="9b7b2-129">В следующем примере показано, как задать байт первого параметра (P1) для [*единицы данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="9b7b2-129">The following example shows how to set the first parameter (P1) byte of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="9b7b2-130">В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="9b7b2-130">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the P1 byte.
hr = pISCardCmd->put_P1(0x06);
if (FAILED(hr))
{
  printf("Failed put_P1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="9b7b2-131">Требования</span><span class="sxs-lookup"><span data-stu-id="9b7b2-131">Requirements</span></span>



| <span data-ttu-id="9b7b2-132">Требование</span><span class="sxs-lookup"><span data-stu-id="9b7b2-132">Requirement</span></span> | <span data-ttu-id="9b7b2-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9b7b2-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b7b2-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b7b2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9b7b2-135">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9b7b2-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9b7b2-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b7b2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9b7b2-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9b7b2-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9b7b2-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="9b7b2-138">End of client support</span></span><br/>    | <span data-ttu-id="9b7b2-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9b7b2-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9b7b2-140">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="9b7b2-140">End of server support</span></span><br/>    | <span data-ttu-id="9b7b2-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9b7b2-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9b7b2-142">Header</span><span class="sxs-lookup"><span data-stu-id="9b7b2-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b7b2-143"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b7b2-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b7b2-144">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="9b7b2-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="9b7b2-145"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9b7b2-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9b7b2-146">DLL</span><span class="sxs-lookup"><span data-stu-id="9b7b2-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b7b2-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b7b2-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9b7b2-148">IID</span><span class="sxs-lookup"><span data-stu-id="9b7b2-148">IID</span></span><br/>                      | <span data-ttu-id="9b7b2-149">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="9b7b2-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="9b7b2-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b7b2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b7b2-151">**получить \_ P1**</span><span class="sxs-lookup"><span data-stu-id="9b7b2-151">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="9b7b2-152">**получить \_ P2**</span><span class="sxs-lookup"><span data-stu-id="9b7b2-152">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="9b7b2-153">**получение \_ P3**</span><span class="sxs-lookup"><span data-stu-id="9b7b2-153">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="9b7b2-154">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="9b7b2-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="9b7b2-155">**разместить \_ P2**</span><span class="sxs-lookup"><span data-stu-id="9b7b2-155">**put\_P2**</span></span>](iscardcmd-put-p2.md)
</dt> </dl>

 

 
