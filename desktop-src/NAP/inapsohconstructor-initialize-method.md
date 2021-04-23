---
title: Метод Initialize Инапсохконструктор (Наппротокол. h)
description: Инициализирует пакет протокола SoH в системе защиты доступа к сети.
ms.assetid: 1678b677-c8c8-465c-a412-9b929e39bbac
keywords:
- Инициализация метода NAP
- Инициализация метода NAP, интерфейс Инапсохконструктор
- Инапсохконструктор интерфейса NAP, метод Initialize
topic_type:
- apiref
api_name:
- INapSoHConstructor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab8d6b27547be6e7c7e9abb59f7edb7b49e716e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988582"
---
# <a name="inapsohconstructorinitialize-method"></a><span data-ttu-id="35154-106">Метод Инапсохконструктор:: Initialize</span><span class="sxs-lookup"><span data-stu-id="35154-106">INapSoHConstructor::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="35154-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="35154-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="35154-108">Метод **инапсохконструктор:: Initialize** инициализирует пакет протокола SoH в системе защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="35154-108">The **INapSoHConstructor::Initialize** method initializes a SoH protocol packet in the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="35154-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35154-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId id,
  [in] BOOL                 isRequest
);
```



## <a name="parameters"></a><span data-ttu-id="35154-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="35154-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35154-111">*идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="35154-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35154-112">Уникальный [системхеалсентитид](nap-datatypes.md) , СОДЕРЖАЩИЙ идентификатор SHA или SHV, который конструирует пакет.</span><span class="sxs-lookup"><span data-stu-id="35154-112">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA or SHV that is constructing the packet.</span></span>

</dd> <dt>

<span data-ttu-id="35154-113">*запрос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35154-113">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35154-114">**Логическое** **значение** , равное true, если пакет должен быть [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) , и **false** , если он должен быть **сохреспонсе**.</span><span class="sxs-lookup"><span data-stu-id="35154-114">A **BOOL** that is **TRUE** if the packet is to be an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is to be an **SoHResponse**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35154-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35154-115">Return value</span></span>

<span data-ttu-id="35154-116">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="35154-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="35154-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="35154-117">Return code</span></span>                                                                                     | <span data-ttu-id="35154-118">Описание</span><span class="sxs-lookup"><span data-stu-id="35154-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="35154-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="35154-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="35154-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="35154-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="35154-121"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="35154-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="35154-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="35154-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="35154-123"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="35154-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="35154-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35154-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="35154-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35154-125">Remarks</span></span>

<span data-ttu-id="35154-126">Этот метод должен вызываться только один раз для каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="35154-126">This method must be called exactly once per packet.</span></span>

<span data-ttu-id="35154-127">[Системхеалсентитид](nap-datatypes.md) , указанный в поле *ID*, является первым TLV в новом пакете SoH и имеет тип атрибута [**сохаттрибутетипесистемхеалсид**](sohattributetype-enum.md).</span><span class="sxs-lookup"><span data-stu-id="35154-127">The [SystemHealthEntityId](nap-datatypes.md) specified in *id*, is the first TLV in the newly constructed SOH packet and has the attribute type [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35154-128">Требования</span><span class="sxs-lookup"><span data-stu-id="35154-128">Requirements</span></span>



| <span data-ttu-id="35154-129">Требование</span><span class="sxs-lookup"><span data-stu-id="35154-129">Requirement</span></span> | <span data-ttu-id="35154-130">Значение</span><span class="sxs-lookup"><span data-stu-id="35154-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="35154-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35154-131">Minimum supported client</span></span><br/> | <span data-ttu-id="35154-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35154-132">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="35154-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35154-133">Minimum supported server</span></span><br/> | <span data-ttu-id="35154-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35154-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="35154-135">Header</span><span class="sxs-lookup"><span data-stu-id="35154-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="35154-136"><dt>Наппротокол. h</dt></span><span class="sxs-lookup"><span data-stu-id="35154-136"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="35154-137">IDL</span><span class="sxs-lookup"><span data-stu-id="35154-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="35154-138"><dt>Наппротокол. idl</dt></span><span class="sxs-lookup"><span data-stu-id="35154-138"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="35154-139">DLL</span><span class="sxs-lookup"><span data-stu-id="35154-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35154-140"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35154-140"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="35154-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35154-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35154-142">**инапсохконструктор**</span><span class="sxs-lookup"><span data-stu-id="35154-142">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





