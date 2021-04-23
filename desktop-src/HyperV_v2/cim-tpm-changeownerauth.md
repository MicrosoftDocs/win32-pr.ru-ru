---
description: Изменяет учетные данные авторизации владельца устройства TPM. Старые и новые пароли авторизации владельца являются обязательными.
ms.assetid: 5b7f1aec-5181-4330-982c-d80a1d5ae9e8
title: Метод Чанжеовнераус класса CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.ChangeOwnerAuth
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2d5a2895e6a0049b2284b55aea1dc9a1849341c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683256"
---
# <a name="changeownerauth-method-of-the-cim_tpm-class"></a><span data-ttu-id="9627c-104">Метод Чанжеовнераус \_ класса TPM CIM</span><span class="sxs-lookup"><span data-stu-id="9627c-104">ChangeOwnerAuth method of the CIM\_TPM class</span></span>

<span data-ttu-id="9627c-105">Изменяет учетные данные авторизации владельца устройства TPM.</span><span class="sxs-lookup"><span data-stu-id="9627c-105">Changes the owner authorization credential of the TPM device.</span></span> <span data-ttu-id="9627c-106">Старые и новые пароли авторизации владельца являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="9627c-106">The old and new owner authorization passwords are required.</span></span>

## <a name="syntax"></a><span data-ttu-id="9627c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9627c-107">Syntax</span></span>


```mof
uint32 ChangeOwnerAuth(
  [in] string OldOwnerAuth,
  [in] string NewOwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="9627c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9627c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9627c-109">*Олдовнераус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9627c-109">*OldOwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9627c-110">Представляет данные авторизации старого владельца, необходимые для получения владения устройством TPM. Подкласс **CIM \_ шаредкредентиал** может требоваться со значением **\_ шаредкредентиал CIM**, отличным от NULL.**Свойство Secret** для параметра.</span><span class="sxs-lookup"><span data-stu-id="9627c-110">Represents the old owner authorization credential required to take ownership of the TPM device.The **CIM\_SharedCredential** subclass may be required with non-null value of the **CIM\_SharedCredential**.**Secret** property for the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9627c-111">*Невовнераус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9627c-111">*NewOwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9627c-112">Представляет учетные данные авторизации нового владельца, необходимые для получения владения устройством TPM. Подкласс **CIM \_ шаредкредентиал** может требоваться со значением **\_ шаредкредентиал CIM**, отличным от NULL.**Свойство Secret** для параметра.</span><span class="sxs-lookup"><span data-stu-id="9627c-112">Represents the new owner authorization credential required to take ownership of the TPM device.The **CIM\_SharedCredential** subclass may be required with non-null value of the **CIM\_SharedCredential**.**Secret** property for the parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9627c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9627c-113">Return value</span></span>

<span data-ttu-id="9627c-114">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="9627c-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="9627c-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="9627c-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9627c-116">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="9627c-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9627c-117">**Неизвестная или Неуказанная ошибка** (2)</span><span class="sxs-lookup"><span data-stu-id="9627c-117">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9627c-118">**Зарезервировано DMTF** (3.. 4095)</span><span class="sxs-lookup"><span data-stu-id="9627c-118">**DMTF Reserved** (3..4095)</span></span>
</dt> <dt>

<span data-ttu-id="9627c-119">**Метод зарезервирован** (4096.. 32767)</span><span class="sxs-lookup"><span data-stu-id="9627c-119">**Method Reserved** (4096..32767)</span></span>
</dt> <dt>

<span data-ttu-id="9627c-120">**Указанный поставщик** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="9627c-120">**Vendor Specified** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9627c-121">Требования</span><span class="sxs-lookup"><span data-stu-id="9627c-121">Requirements</span></span>



| <span data-ttu-id="9627c-122">Требование</span><span class="sxs-lookup"><span data-stu-id="9627c-122">Requirement</span></span> | <span data-ttu-id="9627c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="9627c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9627c-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9627c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9627c-125">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9627c-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9627c-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9627c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9627c-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9627c-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9627c-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9627c-128">Namespace</span></span><br/>                | <span data-ttu-id="9627c-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9627c-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9627c-130">MOF</span><span class="sxs-lookup"><span data-stu-id="9627c-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9627c-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9627c-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9627c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9627c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9627c-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9627c-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9627c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9627c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9627c-135">**\_TPM CIM**</span><span class="sxs-lookup"><span data-stu-id="9627c-135">**CIM\_TPM**</span></span>](cim-tpm.md)
</dt> </dl>

 

 




