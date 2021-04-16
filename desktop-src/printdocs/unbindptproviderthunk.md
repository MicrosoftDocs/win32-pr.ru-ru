---
description: Закрывает маркер поставщика билетов на печать.
ms.assetid: ce979c89-9f9d-4e89-b142-beed414caa3f
title: Функция Унбиндптпровидерсунк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnbindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: dd87f528603624e9957d8c5f3fb12cc857ec4f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693056"
---
# <a name="unbindptproviderthunk-function"></a><span data-ttu-id="d53e4-103">Функция Унбиндптпровидерсунк</span><span class="sxs-lookup"><span data-stu-id="d53e4-103">UnbindPTProviderThunk function</span></span>

<span data-ttu-id="d53e4-104">\[Эта функция не поддерживается и может быть отключена или удалена в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="d53e4-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="d53e4-105">[**Птклосепровидер**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) предоставляет эквивалентную функциональность, и вместо нее следует использовать.\]</span><span class="sxs-lookup"><span data-stu-id="d53e4-105">[**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="d53e4-106">Закрывает маркер поставщика билетов на печать.</span><span class="sxs-lookup"><span data-stu-id="d53e4-106">Closes a handle to a print ticket provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="d53e4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d53e4-107">Syntax</span></span>


```C++
HRESULT UnbindPTProviderThunk(
  _In_ HPTPROVIDER hProvider
);
```



## <a name="parameters"></a><span data-ttu-id="d53e4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d53e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d53e4-109">*хпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d53e4-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d53e4-110">Маркер открытого поставщика билетов на печать.</span><span class="sxs-lookup"><span data-stu-id="d53e4-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="d53e4-111">Этот маркер возвращается функцией [**биндптпровидерсунк**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="d53e4-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d53e4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d53e4-112">Return value</span></span>

<span data-ttu-id="d53e4-113">Если метод завершается успешно, возвращается значение **\_ ОК**. в противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d53e4-113">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="d53e4-114">Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="d53e4-114">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d53e4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d53e4-115">Requirements</span></span>



| <span data-ttu-id="d53e4-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d53e4-116">Requirement</span></span> | <span data-ttu-id="d53e4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d53e4-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d53e4-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d53e4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d53e4-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d53e4-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d53e4-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d53e4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d53e4-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d53e4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d53e4-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d53e4-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d53e4-123"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d53e4-123"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d53e4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d53e4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d53e4-125">Схема печати</span><span class="sxs-lookup"><span data-stu-id="d53e4-125">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="d53e4-126">**птклосепровидер**</span><span class="sxs-lookup"><span data-stu-id="d53e4-126">**PTCloseProvider**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)
</dt> <dt>

[<span data-ttu-id="d53e4-127">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="d53e4-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d53e4-128">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="d53e4-128">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

