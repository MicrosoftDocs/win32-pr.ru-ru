---
description: Извлекает байт второго параметра (P2) из блока данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: c719786f-0f50-472e-a92e-a64c333fc255
title: 'Метод Искардкмд:: get_P2 (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7811ad3e42264477210830f340338d0786ed5547
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145283"
---
# <a name="iscardcmdget_p2-method"></a><span data-ttu-id="63472-103">Метод Искардкмд:: Get \_ P2</span><span class="sxs-lookup"><span data-stu-id="63472-103">ISCardCmd::get\_P2 method</span></span>

<span data-ttu-id="63472-104">\[Метод **Get \_ P2** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="63472-104">\[The **get\_P2** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="63472-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="63472-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="63472-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="63472-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="63472-107">Метод **Get \_ P2** извлекает байт второго параметра (P2) из [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="63472-107">The **get\_P2** method retrieves the second parameter (P2) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="63472-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63472-108">Syntax</span></span>


```C++
HRESULT get_P2(
  [out] BYTE *pbyP2
);
```



## <a name="parameters"></a><span data-ttu-id="63472-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="63472-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63472-110">*pbyP2* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="63472-110">*pbyP2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63472-111">Указатель на байт, который является P2 из КАТЕГОРИЯХ APDU при возврате.</span><span class="sxs-lookup"><span data-stu-id="63472-111">Pointer to the byte that is the P2 from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63472-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63472-112">Return value</span></span>

<span data-ttu-id="63472-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="63472-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="63472-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="63472-114">Return code</span></span>                                                                                   | <span data-ttu-id="63472-115">Описание</span><span class="sxs-lookup"><span data-stu-id="63472-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="63472-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="63472-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="63472-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="63472-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="63472-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="63472-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="63472-119">Недопустимый параметр *pbyP2* .</span><span class="sxs-lookup"><span data-stu-id="63472-119">The *pbyP2* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="63472-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="63472-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="63472-121">В *pbyP2* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="63472-121">A bad pointer was passed in *pbyP2*.</span></span><br/> |
| <dl> <span data-ttu-id="63472-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="63472-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="63472-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="63472-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="63472-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63472-124">Remarks</span></span>

<span data-ttu-id="63472-125">Чтобы присвоить параметру P2 новое значение, вызовите метод [**помещает \_ P2**](iscardcmd-put-p2.md).</span><span class="sxs-lookup"><span data-stu-id="63472-125">To set the P2 parameter to a new value, call [**put\_P2**](iscardcmd-put-p2.md).</span></span>

<span data-ttu-id="63472-126">Чтобы получить параметры P1 или P3, вызовите [**Get \_ P1**](iscardcmd-get-p1.md) и [**Get \_ P3**](iscardcmd-get-p3.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="63472-126">To get the P1 or P3 parameters, call [**get\_P1**](iscardcmd-get-p1.md) and [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="63472-127">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="63472-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="63472-128">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="63472-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="63472-129">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="63472-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="63472-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="63472-130">Examples</span></span>

<span data-ttu-id="63472-131">В следующем примере показано, как получить байт второго параметра (P2) из [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="63472-131">The following example shows how to retrieve the second parameter (P2) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="63472-132">В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="63472-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byP2;
HRESULT  hr;

// Retrieve the P2 byte.
hr = pISCardCmd->get_P2(&byP2);
if (FAILED(hr))
{
  printf("Failed get_P2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="63472-133">Требования</span><span class="sxs-lookup"><span data-stu-id="63472-133">Requirements</span></span>



| <span data-ttu-id="63472-134">Требование</span><span class="sxs-lookup"><span data-stu-id="63472-134">Requirement</span></span> | <span data-ttu-id="63472-135">Значение</span><span class="sxs-lookup"><span data-stu-id="63472-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63472-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63472-136">Minimum supported client</span></span><br/> | <span data-ttu-id="63472-137">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="63472-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="63472-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63472-138">Minimum supported server</span></span><br/> | <span data-ttu-id="63472-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="63472-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="63472-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="63472-140">End of client support</span></span><br/>    | <span data-ttu-id="63472-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="63472-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="63472-142">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="63472-142">End of server support</span></span><br/>    | <span data-ttu-id="63472-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="63472-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="63472-144">Header</span><span class="sxs-lookup"><span data-stu-id="63472-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="63472-145"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="63472-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="63472-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="63472-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="63472-147"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="63472-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="63472-148">DLL</span><span class="sxs-lookup"><span data-stu-id="63472-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63472-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63472-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="63472-150">IID</span><span class="sxs-lookup"><span data-stu-id="63472-150">IID</span></span><br/>                      | <span data-ttu-id="63472-151">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="63472-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="63472-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63472-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63472-153">**получить \_ P1**</span><span class="sxs-lookup"><span data-stu-id="63472-153">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="63472-154">**получение \_ P3**</span><span class="sxs-lookup"><span data-stu-id="63472-154">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="63472-155">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="63472-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="63472-156">**разместить \_ P2**</span><span class="sxs-lookup"><span data-stu-id="63472-156">**put\_P2**</span></span>](iscardcmd-put-p2.md)
</dt> </dl>

 

 
