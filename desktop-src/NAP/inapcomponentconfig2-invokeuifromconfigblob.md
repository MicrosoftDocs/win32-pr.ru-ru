---
title: Метод INapComponentConfig2 Инвокеуифромконфигблоб (Напкоммон. h)
description: Реализуется средствами проверки работоспособности системы (SHV), необходимыми для загрузки конфигурации удаленного или локального компьютера в памяти и вывода пользовательского интерфейса, позволяющего манипулировать данными конфигурации.
ms.assetid: 9c012690-6751-4a47-8683-74abac610c77
keywords:
- Метод Инвокеуифромконфигблоб NAP
- Метод Инвокеуифромконфигблоб NAP, интерфейс INapComponentConfig2
- INapComponentConfig2 интерфейса NAP, метод Инвокеуифромконфигблоб
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIFromConfigBlob
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54cc1efaf7da3434e1aff10d57c2e175481a3d2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891690"
---
# <a name="inapcomponentconfig2invokeuifromconfigblob-method"></a><span data-ttu-id="35d8f-106">Метод INapComponentConfig2:: Инвокеуифромконфигблоб</span><span class="sxs-lookup"><span data-stu-id="35d8f-106">INapComponentConfig2::InvokeUIFromConfigBlob method</span></span>

> [!Note]  
> <span data-ttu-id="35d8f-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="35d8f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="35d8f-108">Метод **инвокеуифромконфигблоб** реализуется средствами проверки работоспособности системы (SHV), необходимыми для загрузки конфигурации удаленного или локального компьютера в памяти и вывода пользовательского интерфейса, позволяющего манипулировать данными конфигурации.</span><span class="sxs-lookup"><span data-stu-id="35d8f-108">The **InvokeUIFromConfigBlob** method is implemented by system health validators (SHVs) as needed to load the configuration of a remote or local machine in memory and display a UI that allows manipulation of the configuration data.</span></span> <span data-ttu-id="35d8f-109">Компонент конфигурации должен поддерживать использование [**инапкомпонентконфиг**](inapcomponentconfig.md) через DCOM.</span><span class="sxs-lookup"><span data-stu-id="35d8f-109">The configuration component must support the usage of [**INapComponentConfig**](inapcomponentconfig.md) through DCOM.</span></span>

## <a name="syntax"></a><span data-ttu-id="35d8f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35d8f-110">Syntax</span></span>


```C++
HRESULT InvokeUIFromConfigBlob(
  [in, unique] HWND   hwndParent,
  [in]         UINT16 inbCount,
  [in]         BYTE   *inData,
  [out]        UINT16 *outbCount,
  [out]        BYTE   **outdata,
  [out]        BOOL   *fConfigChanged
);
```



## <a name="parameters"></a><span data-ttu-id="35d8f-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="35d8f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35d8f-112">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35d8f-112">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35d8f-113">Маркер родительского окна или окно-владельца.</span><span class="sxs-lookup"><span data-stu-id="35d8f-113">A handle to the parent or owner window.</span></span> <span data-ttu-id="35d8f-114">Необходимо указать допустимый описатель окна.</span><span class="sxs-lookup"><span data-stu-id="35d8f-114">A valid window handle must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="35d8f-115">*инбкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35d8f-115">*inbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35d8f-116">Размер *данных* в байтах.</span><span class="sxs-lookup"><span data-stu-id="35d8f-116">The size, in bytes, of *inData*.</span></span>

</dd> <dt>

<span data-ttu-id="35d8f-117">*данные* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35d8f-117">*inData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35d8f-118">Указатель на буфер, в котором хранятся исходные данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="35d8f-118">A pointer to a buffer that stores the initial configuration data.</span></span> <span data-ttu-id="35d8f-119">Эти данные экспортируются с удаленного или локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="35d8f-119">This data is exported from the remote or local machine.</span></span>

</dd> <dt>

<span data-ttu-id="35d8f-120">*аутбкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="35d8f-120">*outbCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35d8f-121">Размер *данных* в байтах.</span><span class="sxs-lookup"><span data-stu-id="35d8f-121">The size, in bytes, of *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="35d8f-122">*данные* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="35d8f-122">*outdata* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35d8f-123">Указатель на буфер, в котором хранятся данные конфигурации, измененные пользовательским интерфейсом конфигурации SHV.</span><span class="sxs-lookup"><span data-stu-id="35d8f-123">A pointer to a buffer that stores configuration data changed by the SHV configuration user interface.</span></span> <span data-ttu-id="35d8f-124">Эти данные импортируются удаленным или локальным компьютером.</span><span class="sxs-lookup"><span data-stu-id="35d8f-124">This data is imported by the remote or local machine.</span></span>

</dd> <dt>

<span data-ttu-id="35d8f-125">*фконфигчанжед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="35d8f-125">*fConfigChanged* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35d8f-126">Указатель на **логическое** значение, равное **true** , если конфигурация была изменена во время операции пользовательского интерфейса, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="35d8f-126">A pointer to a **BOOL** that is set to **TRUE** if the configuration was changed during the UI operation and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35d8f-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35d8f-127">Return value</span></span>

<span data-ttu-id="35d8f-128">Возвращает значение \_ ОК, если успешно, или один из стандартных кодов ошибок Windows.</span><span class="sxs-lookup"><span data-stu-id="35d8f-128">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="35d8f-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35d8f-129">Remarks</span></span>

<span data-ttu-id="35d8f-130">Если используется для локального компьютера, эту функцию можно использовать для каждой конфигурации SHV политики.</span><span class="sxs-lookup"><span data-stu-id="35d8f-130">If used for a local machine, this function can be used for per policy SHV configuration.</span></span> <span data-ttu-id="35d8f-131">Он предоставляет способ вызова пользовательского интерфейса SHV и изменения существующей конфигурации SHV.</span><span class="sxs-lookup"><span data-stu-id="35d8f-131">It provides a way to invoke an SHV UI and edit an existing SHV configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="35d8f-132">Требования</span><span class="sxs-lookup"><span data-stu-id="35d8f-132">Requirements</span></span>



| <span data-ttu-id="35d8f-133">Требование</span><span class="sxs-lookup"><span data-stu-id="35d8f-133">Requirement</span></span> | <span data-ttu-id="35d8f-134">Значение</span><span class="sxs-lookup"><span data-stu-id="35d8f-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="35d8f-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35d8f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="35d8f-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="35d8f-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="35d8f-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35d8f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="35d8f-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35d8f-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="35d8f-139">Header</span><span class="sxs-lookup"><span data-stu-id="35d8f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="35d8f-140"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="35d8f-140"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="35d8f-141">IDL</span><span class="sxs-lookup"><span data-stu-id="35d8f-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="35d8f-142"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="35d8f-142"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35d8f-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35d8f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d8f-144">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="35d8f-144">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





