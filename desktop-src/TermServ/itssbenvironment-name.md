---
title: Итссбенвиронмент имя свойства
description: Извлекает значение, указывающее имя среды, в которой размещен конечный компьютер.
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Имя свойства службы удаленных рабочих столов
- Свойство Name службы удаленных рабочих столов, интерфейс Итссбенвиронмент
- Службы удаленных рабочих столов интерфейса Итссбенвиронмент, свойство Name
topic_type:
- apiref
api_name:
- ITsSbEnvironment.Name
- ITsSbEnvironment.get_Name
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b5ac2fd725ec07102c08e93b2bfb39dabe701ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988397"
---
# <a name="itssbenvironmentname-property"></a><span data-ttu-id="783df-106">Свойство Итссбенвиронмент:: Name</span><span class="sxs-lookup"><span data-stu-id="783df-106">ITsSbEnvironment::Name property</span></span>

<span data-ttu-id="783df-107">Извлекает значение, указывающее имя среды, в которой размещен конечный компьютер.</span><span class="sxs-lookup"><span data-stu-id="783df-107">Retrieves a value that indicates the name of the environment that hosts the target computer.</span></span>

<span data-ttu-id="783df-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="783df-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="783df-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="783df-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="783df-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="783df-110">Property value</span></span>

<span data-ttu-id="783df-111">Указатель на переменную **BSTR** , содержащую имя среды.</span><span class="sxs-lookup"><span data-stu-id="783df-111">A pointer to a **BSTR** variable that contains the name of the environment.</span></span>

## <a name="remarks"></a><span data-ttu-id="783df-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="783df-112">Remarks</span></span>

<span data-ttu-id="783df-113">Этот метод возвращает строку, которая не используется напрямую компонентом подключение к удаленному рабочему столу Broker (RDCB).</span><span class="sxs-lookup"><span data-stu-id="783df-113">This method returns a string that is not directly used by Remote Desktop Connection Broker (RD Connection Broker).</span></span> <span data-ttu-id="783df-114">RDCB передает эту строку в подключаемые модули ресурсов.</span><span class="sxs-lookup"><span data-stu-id="783df-114">RD Connection Broker passes this string to resource plug-ins.</span></span>

## <a name="requirements"></a><span data-ttu-id="783df-115">Требования</span><span class="sxs-lookup"><span data-stu-id="783df-115">Requirements</span></span>



| <span data-ttu-id="783df-116">Требование</span><span class="sxs-lookup"><span data-stu-id="783df-116">Requirement</span></span> | <span data-ttu-id="783df-117">Значение</span><span class="sxs-lookup"><span data-stu-id="783df-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="783df-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="783df-118">Minimum supported client</span></span><br/> | <span data-ttu-id="783df-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="783df-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="783df-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="783df-120">Minimum supported server</span></span><br/> | <span data-ttu-id="783df-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="783df-121">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="783df-122">IDL</span><span class="sxs-lookup"><span data-stu-id="783df-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="783df-123"><dt>Сбтсв. idl</dt></span><span class="sxs-lookup"><span data-stu-id="783df-123"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="783df-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="783df-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="783df-125">**итссбенвиронмент**</span><span class="sxs-lookup"><span data-stu-id="783df-125">**ITsSbEnvironment**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 





