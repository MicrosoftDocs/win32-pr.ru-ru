---
description: Считывает двоичные данные. Не рекомендуется.
ms.assetid: 530552c5-bf05-4e86-836d-d25161832c6d
title: 'Метод Идиректксфилебинари:: Read (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.Read
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 60548640fbbb0e67909eab1fed2df24a3465bf95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081912"
---
# <a name="idirectxfilebinaryread-method"></a><span data-ttu-id="ac77e-104">Метод Идиректксфилебинари:: Read</span><span class="sxs-lookup"><span data-stu-id="ac77e-104">IDirectXFileBinary::Read method</span></span>

<span data-ttu-id="ac77e-105">Считывает двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="ac77e-105">Reads the binary data.</span></span> <span data-ttu-id="ac77e-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ac77e-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac77e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac77e-107">Syntax</span></span>


```C++
HRESULT Read(
  [out] LPVOID  pvData,
  [in]  DWORD   cbSize,
  [out] LPDWORD pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="ac77e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac77e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac77e-109">*пвдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ac77e-109">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac77e-110">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac77e-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac77e-111">Указатель на буфер, который получает считанные данные.</span><span class="sxs-lookup"><span data-stu-id="ac77e-111">Pointer to the buffer that receives the data that has been read.</span></span>

</dd> <dt>

<span data-ttu-id="ac77e-112">*кбсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac77e-112">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac77e-113">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac77e-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac77e-114">Размер буфера, на который указывает Пвдата, в байтах.</span><span class="sxs-lookup"><span data-stu-id="ac77e-114">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ac77e-115">*пкбреад* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ac77e-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac77e-116">Тип: **[ **лпдворд**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac77e-116">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac77e-117">Указатель на число фактически считанных байтов.</span><span class="sxs-lookup"><span data-stu-id="ac77e-117">Pointer to the number of bytes actually read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac77e-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac77e-118">Return value</span></span>

<span data-ttu-id="ac77e-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ac77e-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ac77e-120">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ac77e-120">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="ac77e-121">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадвалуе, дксфилирр \_ номоредата.</span><span class="sxs-lookup"><span data-stu-id="ac77e-121">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac77e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ac77e-122">Requirements</span></span>



| <span data-ttu-id="ac77e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ac77e-123">Requirement</span></span> | <span data-ttu-id="ac77e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ac77e-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac77e-125">Header</span><span class="sxs-lookup"><span data-stu-id="ac77e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ac77e-126"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac77e-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac77e-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ac77e-127">Library</span></span><br/> | <dl> <span data-ttu-id="ac77e-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac77e-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac77e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac77e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac77e-130">идиректксфилебинари</span><span class="sxs-lookup"><span data-stu-id="ac77e-130">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
