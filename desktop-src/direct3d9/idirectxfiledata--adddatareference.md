---
description: Создает и добавляет объект ссылки на данные в качестве дочернего объекта. Не рекомендуется.
ms.assetid: 71a770a2-1502-4b93-b368-990c3318bd33
title: 'Метод Идиректксфиледата:: Адддатареференце (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataReference
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 44834af51380c3b8bdbb4e9a4b24bf911ea6a07f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713629"
---
# <a name="idirectxfiledataadddatareference-method"></a><span data-ttu-id="d911a-104">Метод Идиректксфиледата:: Адддатареференце</span><span class="sxs-lookup"><span data-stu-id="d911a-104">IDirectXFileData::AddDataReference method</span></span>

<span data-ttu-id="d911a-105">Создает и добавляет объект ссылки на данные в качестве дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="d911a-105">Creates and adds a data reference object as a child object.</span></span> <span data-ttu-id="d911a-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d911a-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d911a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d911a-107">Syntax</span></span>


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szRef,
  [in] const GUID   *pguidRef
);
```



## <a name="parameters"></a><span data-ttu-id="d911a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d911a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d911a-109">*сзреф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d911a-109">*szRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d911a-110">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d911a-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d911a-111">Указатель на имя объекта данных, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="d911a-111">Pointer to the name of the referenced data object.</span></span> <span data-ttu-id="d911a-112">Этот параметр может иметь **значение NULL** , если пгуидреф предоставляет ссылку на идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="d911a-112">This parameter can be **NULL** if pguidRef provides a reference to the GUID.</span></span>

</dd> <dt>

<span data-ttu-id="d911a-113">*пгуидреф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d911a-113">*pguidRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d911a-114">Тип: **константа [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="d911a-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="d911a-115">Указатель на идентификатор GUID, представляющий данные.</span><span class="sxs-lookup"><span data-stu-id="d911a-115">Pointer to the GUID representing the data.</span></span> <span data-ttu-id="d911a-116">Этот параметр может иметь **значение NULL** , если сзреф предоставляет ссылку на имя.</span><span class="sxs-lookup"><span data-stu-id="d911a-116">This parameter can be **NULL** if szRef provides a reference to the name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d911a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d911a-117">Return value</span></span>

<span data-ttu-id="d911a-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d911a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d911a-119">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d911a-119">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="d911a-120">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих значений. ДКСФИЛИРР \_ БАДАЛЛОК дксфилирр \_ бадвалуе</span><span class="sxs-lookup"><span data-stu-id="d911a-120">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="d911a-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d911a-121">Remarks</span></span>

<span data-ttu-id="d911a-122">Чтобы этот метод был выполнен, параметр Сзреф или Пгуидреф должен иметь значение, отличное от **null**.</span><span class="sxs-lookup"><span data-stu-id="d911a-122">For this method to succeed, either the szRef or pguidRef parameter must be non-**NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d911a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d911a-123">Requirements</span></span>



| <span data-ttu-id="d911a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d911a-124">Requirement</span></span> | <span data-ttu-id="d911a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d911a-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d911a-126">Header</span><span class="sxs-lookup"><span data-stu-id="d911a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d911a-127"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="d911a-127"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="d911a-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d911a-128">Library</span></span><br/> | <dl> <span data-ttu-id="d911a-129"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d911a-129"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d911a-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d911a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d911a-131">идиректксфиледата</span><span class="sxs-lookup"><span data-stu-id="d911a-131">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> </dl>

 

 
