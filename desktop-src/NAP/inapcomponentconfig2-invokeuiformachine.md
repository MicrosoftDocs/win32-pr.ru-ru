---
title: Метод INapComponentConfig2 Инвокеуиформачине (Напкоммон. h)
description: Реализуется средствами проверки работоспособности системы (SHV), необходимыми для управления удаленной конфигурацией непосредственно на указанном компьютере. Этот метод запускает пользовательский интерфейс управления конфигурацией.
ms.assetid: 67a6d715-250b-4b8b-9c27-8173926b7bfe
keywords:
- Метод Инвокеуиформачине NAP
- Метод Инвокеуиформачине NAP, интерфейс INapComponentConfig2
- INapComponentConfig2 интерфейса NAP, метод Инвокеуиформачине
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIForMachine
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bc0c09f802a63a5bfad92b49f76fcbb4ee242d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135774"
---
# <a name="inapcomponentconfig2invokeuiformachine-method"></a><span data-ttu-id="cd531-107">Метод INapComponentConfig2:: Инвокеуиформачине</span><span class="sxs-lookup"><span data-stu-id="cd531-107">INapComponentConfig2::InvokeUIForMachine method</span></span>

> [!Note]  
> <span data-ttu-id="cd531-108">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="cd531-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="cd531-109">Метод **инвокеуиформачине** реализуется средствами проверки работоспособности системы (SHV), необходимыми для управления удаленной конфигурацией непосредственно на указанном компьютере.</span><span class="sxs-lookup"><span data-stu-id="cd531-109">The **InvokeUIForMachine** method is implemented by system health validators (SHVs) as needed to manage remote configuration directly on the machine specified.</span></span> <span data-ttu-id="cd531-110">Этот метод запускает пользовательский интерфейс управления конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="cd531-110">This method launches a configuration management UI.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd531-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd531-111">Syntax</span></span>


```C++
HRESULT InvokeUIForMachine(
  [in] HWND          hwndParent,
  [in] CountedString *machineName
);
```



## <a name="parameters"></a><span data-ttu-id="cd531-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd531-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd531-113">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd531-113">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd531-114">Маркер родительского окна или окно-владельца.</span><span class="sxs-lookup"><span data-stu-id="cd531-114">A handle to the parent or owner window.</span></span> <span data-ttu-id="cd531-115">Необходимо указать допустимый описатель окна.</span><span class="sxs-lookup"><span data-stu-id="cd531-115">A valid window handle must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="cd531-116">*MachineName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd531-116">*machineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd531-117">Указатель на [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , содержащий имя компьютера клиента NAP.</span><span class="sxs-lookup"><span data-stu-id="cd531-117">A pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) that contains the machine name of the NAP client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd531-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd531-118">Return value</span></span>

<span data-ttu-id="cd531-119">Возвращает значение \_ ОК, если успешно, или один из стандартных кодов ошибок Windows.</span><span class="sxs-lookup"><span data-stu-id="cd531-119">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd531-120">Требования</span><span class="sxs-lookup"><span data-stu-id="cd531-120">Requirements</span></span>



| <span data-ttu-id="cd531-121">Требование</span><span class="sxs-lookup"><span data-stu-id="cd531-121">Requirement</span></span> | <span data-ttu-id="cd531-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cd531-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd531-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd531-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cd531-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cd531-124">None supported</span></span><br/>                                                                |
| <span data-ttu-id="cd531-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd531-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cd531-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cd531-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cd531-127">Header</span><span class="sxs-lookup"><span data-stu-id="cd531-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd531-128"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd531-128"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd531-129">IDL</span><span class="sxs-lookup"><span data-stu-id="cd531-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cd531-130"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cd531-130"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd531-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd531-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd531-132">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="cd531-132">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





