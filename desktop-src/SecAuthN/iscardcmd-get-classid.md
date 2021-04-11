---
description: Извлекает идентификатор класса из блока данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: 03ea997d-7698-43c7-aa9a-dfc1bac6fcdd
title: 'Метод Искардкмд:: get_ClassId (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6b78dfc9f3adf200a614b129ff1e86a16c88438f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145295"
---
# <a name="iscardcmdget_classid-method"></a><span data-ttu-id="af8c1-103">Метод Искардкмд:: Get \_ ClassID</span><span class="sxs-lookup"><span data-stu-id="af8c1-103">ISCardCmd::get\_ClassId method</span></span>

<span data-ttu-id="af8c1-104">\[Метод **Get \_ ClassID** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="af8c1-104">\[The **get\_ClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="af8c1-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="af8c1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="af8c1-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="af8c1-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="af8c1-107">Метод **Get \_ ClassID** извлекает идентификатор класса из [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="af8c1-107">The **get\_ClassId** method retrieves the class identifier from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="af8c1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af8c1-108">Syntax</span></span>


```C++
HRESULT get_ClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a><span data-ttu-id="af8c1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="af8c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af8c1-110">*пбикласс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="af8c1-110">*pbyClass* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af8c1-111">Указатель на байт, представляющий идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="af8c1-111">Pointer to the byte that represents the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af8c1-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af8c1-112">Return value</span></span>

<span data-ttu-id="af8c1-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="af8c1-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="af8c1-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="af8c1-114">Return code</span></span>                                                                                   | <span data-ttu-id="af8c1-115">Описание</span><span class="sxs-lookup"><span data-stu-id="af8c1-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="af8c1-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="af8c1-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="af8c1-117">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="af8c1-117">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="af8c1-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="af8c1-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="af8c1-119">Недопустимый параметр *пбикласс* .</span><span class="sxs-lookup"><span data-stu-id="af8c1-119">The *pbyClass* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="af8c1-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="af8c1-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="af8c1-121">В *пбикласс* был передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="af8c1-121">A bad pointer was passed in *pbyClass*.</span></span><br/> |
| <dl> <span data-ttu-id="af8c1-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="af8c1-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="af8c1-123">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="af8c1-123">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="af8c1-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af8c1-124">Remarks</span></span>

<span data-ttu-id="af8c1-125">Чтобы задать новое значение идентификатора класса, вызовите метод Set [**\_ ClassID**](iscardcmd-put-classid.md).</span><span class="sxs-lookup"><span data-stu-id="af8c1-125">To set the class identifier to a new value, call [**put\_ClassId**](iscardcmd-put-classid.md).</span></span>

<span data-ttu-id="af8c1-126">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="af8c1-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="af8c1-127">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="af8c1-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="af8c1-128">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="af8c1-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="af8c1-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="af8c1-129">Examples</span></span>

<span data-ttu-id="af8c1-130">В следующем примере показано, как получить идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="af8c1-130">The following example shows how to retrieve the class ID.</span></span> <span data-ttu-id="af8c1-131">В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="af8c1-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     byClassID;
HRESULT  hr;

// Retrieve the class ID.
hr = pISCardCmd->get_ClassId(&byClassID);
if (FAILED(hr))
{
  printf("Failed get_ClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="af8c1-132">Требования</span><span class="sxs-lookup"><span data-stu-id="af8c1-132">Requirements</span></span>



| <span data-ttu-id="af8c1-133">Требование</span><span class="sxs-lookup"><span data-stu-id="af8c1-133">Requirement</span></span> | <span data-ttu-id="af8c1-134">Значение</span><span class="sxs-lookup"><span data-stu-id="af8c1-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af8c1-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af8c1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="af8c1-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="af8c1-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="af8c1-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af8c1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="af8c1-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af8c1-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="af8c1-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="af8c1-139">End of client support</span></span><br/>    | <span data-ttu-id="af8c1-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="af8c1-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="af8c1-141">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="af8c1-141">End of server support</span></span><br/>    | <span data-ttu-id="af8c1-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af8c1-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="af8c1-143">Header</span><span class="sxs-lookup"><span data-stu-id="af8c1-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="af8c1-144"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="af8c1-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="af8c1-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="af8c1-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="af8c1-146"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="af8c1-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="af8c1-147">DLL</span><span class="sxs-lookup"><span data-stu-id="af8c1-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af8c1-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af8c1-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="af8c1-149">IID</span><span class="sxs-lookup"><span data-stu-id="af8c1-149">IID</span></span><br/>                      | <span data-ttu-id="af8c1-150">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="af8c1-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="af8c1-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af8c1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af8c1-152">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="af8c1-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="af8c1-153">**Размещение \_ ClassID**</span><span class="sxs-lookup"><span data-stu-id="af8c1-153">**put\_ClassId**</span></span>](iscardcmd-put-classid.md)
</dt> </dl>

 

 
