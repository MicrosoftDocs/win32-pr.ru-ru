---
description: Возвращает поле Le блока данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: 249e8105-273b-42f0-9427-9b3cda5bf0a1
title: 'Метод Искардкмд:: get_LeField (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_LeField
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bc35f2686a32ce07e1ca630d3ccad3c47b36ca2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818505"
---
# <a name="iscardcmdget_lefield-method"></a><span data-ttu-id="0e425-103">Метод Искардкмд:: Get \_ лефиелд</span><span class="sxs-lookup"><span data-stu-id="0e425-103">ISCardCmd::get\_LeField method</span></span>

<span data-ttu-id="0e425-104">\[Метод **Get \_ лефиелд** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="0e425-104">\[The **get\_LeField** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0e425-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0e425-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0e425-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="0e425-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0e425-107">Метод **Get \_ лефиелд** возвращает поле Le [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="0e425-107">The **get\_LeField** method returns the Le field of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="0e425-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e425-108">Syntax</span></span>


```C++
HRESULT get_LeField(
  [out] LONG *plSize
);
```



## <a name="parameters"></a><span data-ttu-id="0e425-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e425-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e425-110">*плсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0e425-110">*plSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e425-111">Указатель на значение поля Le при возврате.</span><span class="sxs-lookup"><span data-stu-id="0e425-111">Pointer to the Le field value on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e425-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e425-112">Return value</span></span>

<span data-ttu-id="0e425-113">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="0e425-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="0e425-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0e425-114">Return code</span></span>                                                                                  | <span data-ttu-id="0e425-115">Описание</span><span class="sxs-lookup"><span data-stu-id="0e425-115">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="0e425-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0e425-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0e425-117">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="0e425-117">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="0e425-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0e425-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0e425-119">Недопустимый параметр *плсизе* .</span><span class="sxs-lookup"><span data-stu-id="0e425-119">The *plSize* parameter is not valid.</span></span><br/>  |



 

## <a name="examples"></a><span data-ttu-id="0e425-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="0e425-120">Examples</span></span>

<span data-ttu-id="0e425-121">В следующем примере показано, как получить значение поля Le из [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).</span><span class="sxs-lookup"><span data-stu-id="0e425-121">The following example shows how to retrieve the Le field value from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="0e425-122">В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="0e425-122">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
LONG     lLe;
HRESULT  hr;

// Retrieve the Le field value.
hr = pISCardCmd->get_LeField(&lLe);
if (FAILED(hr))
{
    printf("Failed get_LeField\n");
    // Take other error handling action.
}
else
    printf("Le field value returned is %d\n", lLe);
```



## <a name="requirements"></a><span data-ttu-id="0e425-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0e425-123">Requirements</span></span>



| <span data-ttu-id="0e425-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0e425-124">Requirement</span></span> | <span data-ttu-id="0e425-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0e425-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e425-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e425-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0e425-127">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0e425-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0e425-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e425-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0e425-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0e425-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0e425-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0e425-130">End of client support</span></span><br/>    | <span data-ttu-id="0e425-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0e425-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="0e425-132">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="0e425-132">End of server support</span></span><br/>    | <span data-ttu-id="0e425-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0e425-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="0e425-134">Header</span><span class="sxs-lookup"><span data-stu-id="0e425-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e425-135"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e425-135"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e425-136">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0e425-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="0e425-137"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0e425-137"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0e425-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0e425-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e425-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e425-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0e425-140">IID</span><span class="sxs-lookup"><span data-stu-id="0e425-140">IID</span></span><br/>                      | <span data-ttu-id="0e425-141">IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="0e425-141">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0e425-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e425-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e425-143">**искардкмд**</span><span class="sxs-lookup"><span data-stu-id="0e425-143">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
