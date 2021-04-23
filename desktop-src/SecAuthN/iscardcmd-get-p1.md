---
description: Извлекает байт первого параметра (P1) из блока данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: a6648e70-96d8-4b7d-ae6d-8832e38d1c71
title: 'Метод Искардкмд:: get_P1 (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 047732fd8602828cc0501d623c57653bfdc9044f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541831"
---
# <a name="iscardcmdget_p1-method"></a><span data-ttu-id="f708b-103">Метод Искардкмд:: Get \_ P1</span><span class="sxs-lookup"><span data-stu-id="f708b-103">ISCardCmd::get\_P1 method</span></span>

<span data-ttu-id="f708b-104">\[Метод **Get \_ P1** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="f708b-104">\[The **get\_P1** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f708b-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f708b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f708b-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="f708b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f708b-107">Метод **Get \_ P1** извлекает байт первого параметра (P1) из [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="f708b-107">The **get\_P1** method retrieves the first parameter (P1) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="f708b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f708b-108">Syntax</span></span>


```C++
HRESULT get_P1(
  [out] BYTE *pbyP1
);
```



## <a name="parameters"></a><span data-ttu-id="f708b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f708b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f708b-110">*pbyP1* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f708b-110">*pbyP1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f708b-111">Указатель на байт P1 в КАТЕГОРИЯХ APDU при возврате.</span><span class="sxs-lookup"><span data-stu-id="f708b-111">Pointer to the P1 byte in the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f708b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f708b-112">Return value</span></span>

<span data-ttu-id="f708b-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="f708b-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="f708b-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f708b-114">Return code</span></span>                                                                                   | <span data-ttu-id="f708b-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f708b-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="f708b-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f708b-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f708b-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="f708b-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="f708b-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f708b-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f708b-119">Недопустимый параметр *pbyP1* .</span><span class="sxs-lookup"><span data-stu-id="f708b-119">The *pbyP1* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="f708b-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="f708b-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f708b-121">В *pbyP1* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="f708b-121">A bad pointer was passed in *pbyP1*.</span></span><br/> |
| <dl> <span data-ttu-id="f708b-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f708b-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f708b-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="f708b-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="f708b-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f708b-124">Remarks</span></span>

<span data-ttu-id="f708b-125">Чтобы присвоить параметру P1 новое значение, вызовите метод Set [**\_ P1**](iscardcmd-put-p1.md).</span><span class="sxs-lookup"><span data-stu-id="f708b-125">To set the P1 parameter to a new value, call [**put\_P1**](iscardcmd-put-p1.md).</span></span>

<span data-ttu-id="f708b-126">Чтобы получить параметры P2 или P3, вызовите [**Get \_ P2**](iscardcmd-get-p2.md) и [**Get \_ P3**](iscardcmd-get-p3.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="f708b-126">To get the P2 or P3 parameters, call [**get\_P2**](iscardcmd-get-p2.md) and [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="f708b-127">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="f708b-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="f708b-128">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="f708b-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="f708b-129">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f708b-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f708b-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="f708b-130">Examples</span></span>

<span data-ttu-id="f708b-131">В следующем примере показано, как получить байт первого параметра (P1) из [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="f708b-131">The following example shows how to retrieve the first parameter (P1) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="f708b-132">В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="f708b-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byP1;
HRESULT  hr;

// Retrieve the P1 byte.
hr = pISCardCmd->get_P1(&byP1);
if (FAILED(hr))
{
  printf("Failed get_P1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="f708b-133">Требования</span><span class="sxs-lookup"><span data-stu-id="f708b-133">Requirements</span></span>



| <span data-ttu-id="f708b-134">Требование</span><span class="sxs-lookup"><span data-stu-id="f708b-134">Requirement</span></span> | <span data-ttu-id="f708b-135">Значение</span><span class="sxs-lookup"><span data-stu-id="f708b-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f708b-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f708b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f708b-137">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f708b-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f708b-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f708b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f708b-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f708b-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f708b-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f708b-140">End of client support</span></span><br/>    | <span data-ttu-id="f708b-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f708b-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f708b-142">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f708b-142">End of server support</span></span><br/>    | <span data-ttu-id="f708b-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f708b-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f708b-144">Header</span><span class="sxs-lookup"><span data-stu-id="f708b-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f708b-145"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="f708b-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="f708b-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f708b-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="f708b-147"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f708b-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f708b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="f708b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f708b-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f708b-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f708b-150">IID</span><span class="sxs-lookup"><span data-stu-id="f708b-150">IID</span></span><br/>                      | <span data-ttu-id="f708b-151">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="f708b-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="f708b-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f708b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f708b-153">**получить \_ P2**</span><span class="sxs-lookup"><span data-stu-id="f708b-153">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="f708b-154">**получение \_ P3**</span><span class="sxs-lookup"><span data-stu-id="f708b-154">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="f708b-155">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="f708b-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="f708b-156">**разместить \_ P1**</span><span class="sxs-lookup"><span data-stu-id="f708b-156">**put\_P1**</span></span>](iscardcmd-put-p1.md)
</dt> </dl>

 

 
