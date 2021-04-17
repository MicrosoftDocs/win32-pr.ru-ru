---
title: ITSRemoteProgram3 Серверстартапп, метод
description: Указывает приложение, запускаемое в удаленном сеансе.
ms.assetid: 55a05d05-66d5-48a1-b3a6-f087aeb62925
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Серверстартапп
- Службы удаленных рабочих столов метода Серверстартапп, интерфейс ITSRemoteProgram3
- Службы удаленных рабочих столов интерфейса ITSRemoteProgram3, метод Серверстартапп
topic_type:
- apiref
api_name:
- ITSRemoteProgram3.ServerStartApp
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1822fa98094870ebebe607528cdc69a8a201f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682077"
---
# <a name="itsremoteprogram3serverstartapp-method"></a><span data-ttu-id="4095a-106">Метод ITSRemoteProgram3:: Серверстартапп</span><span class="sxs-lookup"><span data-stu-id="4095a-106">ITSRemoteProgram3::ServerStartApp method</span></span>

<span data-ttu-id="4095a-107">Указывает приложение, запускаемое в удаленном сеансе.</span><span class="sxs-lookup"><span data-stu-id="4095a-107">Specifies an App to start in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="4095a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4095a-108">Syntax</span></span>


```C++
HRESULT ServerStartApp(
  [in] BSTR         bstrAppUserModelId,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a><span data-ttu-id="4095a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4095a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4095a-110">*бстраппусермоделид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4095a-110">*bstrAppUserModelId* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="4095a-111">*бстраргументс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4095a-111">*bstrArguments* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="4095a-112">*вбекспанденвваринаргументсонсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4095a-112">*vbExpandEnvVarInArgumentsOnServer* \[in\]</span></span>
<span data-ttu-id="4095a-113"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4095a-113"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="4095a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4095a-114">Return value</span></span>

<span data-ttu-id="4095a-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4095a-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4095a-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4095a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4095a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4095a-117">Requirements</span></span>



| <span data-ttu-id="4095a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4095a-118">Requirement</span></span> | <span data-ttu-id="4095a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4095a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4095a-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4095a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4095a-121">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4095a-121">Windows 10 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4095a-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4095a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4095a-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4095a-123">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="4095a-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4095a-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="4095a-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4095a-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4095a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4095a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4095a-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4095a-127"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4095a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4095a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4095a-129">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="4095a-129">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> </dl>

 

 





