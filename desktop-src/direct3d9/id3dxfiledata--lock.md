---
description: Обращается к данным файла. x.
ms.assetid: 0e92914b-47b3-4a88-87ba-ce3c14282dbb
title: 'Метод ID3DXFileData:: Lock (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Lock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 27ef18fcb12b00f0b778ee15d582610ffe52fe54
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713801"
---
# <a name="id3dxfiledatalock-method"></a><span data-ttu-id="1098d-103">Метод ID3DXFileData:: Lock</span><span class="sxs-lookup"><span data-stu-id="1098d-103">ID3DXFileData::Lock method</span></span>

<span data-ttu-id="1098d-104">Обращается к данным файла. x.</span><span class="sxs-lookup"><span data-stu-id="1098d-104">Accesses the .x file data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1098d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1098d-105">Syntax</span></span>


```C++
HRESULT Lock(
  [in]       SIZE_T *pSize,
  [in] const VOID   **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="1098d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1098d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1098d-107">*псизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1098d-107">*pSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1098d-108">Type: **[ **size \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1098d-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1098d-109">Указатель на размер данных файла. x.</span><span class="sxs-lookup"><span data-stu-id="1098d-109">Pointer to the size of the .x file data.</span></span>

</dd> <dt>

<span data-ttu-id="1098d-110">*ппдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1098d-110">*ppData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1098d-111">Тип: **константа \* \* void**</span><span class="sxs-lookup"><span data-stu-id="1098d-111">Type: **const VOID\*\***</span></span>

<span data-ttu-id="1098d-112">Адрес указателя для получения указателя интерфейса объекта данных [**ID3DXFileData**](id3dxfiledata.md) File.</span><span class="sxs-lookup"><span data-stu-id="1098d-112">Address of a pointer to receive the [**ID3DXFileData**](id3dxfiledata.md) file data object's interface pointer.</span></span> <span data-ttu-id="1098d-113">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="1098d-113">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1098d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1098d-114">Return value</span></span>

<span data-ttu-id="1098d-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1098d-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1098d-116">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="1098d-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1098d-117">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="1098d-117">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="1098d-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1098d-118">Remarks</span></span>

<span data-ttu-id="1098d-119">Указатель *ппдата* допустим только во время **ID3DXFileData:: Lock** ... Последовательность [**ID3DXFileData:: Unlock**](id3dxfiledata--unlock.md) .</span><span class="sxs-lookup"><span data-stu-id="1098d-119">The *ppData* pointer is only valid during a **ID3DXFileData::Lock** ... [**ID3DXFileData::Unlock**](id3dxfiledata--unlock.md) sequence.</span></span> <span data-ttu-id="1098d-120">Можно выполнить несколько вызовов блокировок.</span><span class="sxs-lookup"><span data-stu-id="1098d-120">You can make multiple lock calls.</span></span> <span data-ttu-id="1098d-121">Однако необходимо убедиться, что количество вызовов блокировок соответствует числу вызовов Unlock.</span><span class="sxs-lookup"><span data-stu-id="1098d-121">However, you must ensure that the number of lock calls matches the number of unlock calls.</span></span>

<span data-ttu-id="1098d-122">Так как данные файлов не гарантированно правильно согласованы с границами байтов, доступ к *ппдата* должен осуществляться с помощью несогласованных указателей.</span><span class="sxs-lookup"><span data-stu-id="1098d-122">Because file data is not guaranteed to be aligned properly with byte boundaries, you should access *ppData* with UNALIGNED pointers.</span></span>

<span data-ttu-id="1098d-123">Возвращаемые значения параметров не обязательно должны быть допустимы из-за возможного повреждения файла; Поэтому код должен проверять возвращаемые значения параметров.</span><span class="sxs-lookup"><span data-stu-id="1098d-123">Returned parameter values are not guaranteed to be valid due to possible file corruption; therefore, your code should verify the returned parameter values.</span></span>

## <a name="requirements"></a><span data-ttu-id="1098d-124">Требования</span><span class="sxs-lookup"><span data-stu-id="1098d-124">Requirements</span></span>



| <span data-ttu-id="1098d-125">Требование</span><span class="sxs-lookup"><span data-stu-id="1098d-125">Requirement</span></span> | <span data-ttu-id="1098d-126">Значение</span><span class="sxs-lookup"><span data-stu-id="1098d-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1098d-127">Header</span><span class="sxs-lookup"><span data-stu-id="1098d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="1098d-128"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="1098d-128"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="1098d-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1098d-129">Library</span></span><br/> | <dl> <span data-ttu-id="1098d-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1098d-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1098d-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1098d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1098d-132">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="1098d-132">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
