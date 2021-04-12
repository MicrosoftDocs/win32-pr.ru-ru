---
title: Итссбклиентконнектион, свойство среды
description: Извлекает объект, содержащий сведения о среде, в которой размещен конечный компьютер.
ms.assetid: 97fe4851-96a9-4b23-8ad7-f42b87c655d0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства среды
- Свойство окружения службы удаленных рабочих столов, интерфейс Итссбклиентконнектион
- Службы удаленных рабочих столов интерфейса Итссбклиентконнектион, свойство Environment
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Environment
- ITsSbClientConnection.get_Environment
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18018c8f8fc5e7d017809cf5fe109db7c52712c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491616"
---
# <a name="itssbclientconnectionenvironment-property"></a><span data-ttu-id="d417e-106">Свойство Итссбклиентконнектион:: Environment</span><span class="sxs-lookup"><span data-stu-id="d417e-106">ITsSbClientConnection::Environment property</span></span>

<span data-ttu-id="d417e-107">Извлекает объект, содержащий сведения о среде, в которой размещен конечный компьютер.</span><span class="sxs-lookup"><span data-stu-id="d417e-107">Retrieves an object that contains information about the environment that hosts the target computer.</span></span> <span data-ttu-id="d417e-108">Например, в сценарии виртуального рабочего стола этот объект будет содержать сведения о компьютере, на котором размещена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="d417e-108">For example, in a virtual desktop scenario, this object would contain information about the computer that hosts the virtual machine.</span></span>

<span data-ttu-id="d417e-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d417e-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d417e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d417e-110">Syntax</span></span>


```C++
HRESULT get_Environment(
  [out, retval] ITsSbEnvironment **ppEnvironment
);
```



## <a name="property-value"></a><span data-ttu-id="d417e-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d417e-111">Property value</span></span>

<span data-ttu-id="d417e-112">Указатель на указатель на объект среды [**итссбенвиронмент**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) .</span><span class="sxs-lookup"><span data-stu-id="d417e-112">A pointer to a pointer to an [**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) environment object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d417e-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d417e-113">Error codes</span></span>

<span data-ttu-id="d417e-114">Если метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d417e-114">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d417e-115">В противном случае возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="d417e-115">Otherwise, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="d417e-116">Возможные значения включают, но не ограничиваются, перечисленные в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="d417e-116">Possible values include, but are not limited to, those in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d417e-117">\_указатель E</span><span class="sxs-lookup"><span data-stu-id="d417e-117">E\_POINTER</span></span>
</dt> <dd>

<span data-ttu-id="d417e-118">Среда не найдена.</span><span class="sxs-lookup"><span data-stu-id="d417e-118">The environment was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d417e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d417e-119">Remarks</span></span>

<span data-ttu-id="d417e-120">Подключаемый модуль оркестрации может вызывать этот метод для получения сведений о среде для целевой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d417e-120">An orchestration plug-in can call this method to retrieve environment information about a target virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="d417e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d417e-121">Requirements</span></span>



| <span data-ttu-id="d417e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d417e-122">Requirement</span></span> | <span data-ttu-id="d417e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d417e-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d417e-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d417e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d417e-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d417e-125">None supported</span></span><br/>                                                            |
| <span data-ttu-id="d417e-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d417e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d417e-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d417e-127">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="d417e-128">IDL</span><span class="sxs-lookup"><span data-stu-id="d417e-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d417e-129"><dt>Сбтсв. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d417e-129"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d417e-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d417e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d417e-131">**итссбклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="d417e-131">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

 





