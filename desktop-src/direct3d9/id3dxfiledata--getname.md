---
description: Извлекает имя этого файлового объекта данных.
ms.assetid: 182529cb-144c-4ed8-94bf-6688598e9ea7
title: Метод ID3DXFileData::-Name (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e27fc3e95280f29a33d4ececffc7c229563462a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713802"
---
# <a name="id3dxfiledatagetname-method"></a><span data-ttu-id="3ca4e-103">Метод ID3DXFileData:: Name</span><span class="sxs-lookup"><span data-stu-id="3ca4e-103">ID3DXFileData::GetName method</span></span>

<span data-ttu-id="3ca4e-104">Извлекает имя этого файлового объекта данных.</span><span class="sxs-lookup"><span data-stu-id="3ca4e-104">Retrieves the name of this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ca4e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ca4e-105">Syntax</span></span>


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a><span data-ttu-id="3ca4e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ca4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ca4e-107">*szName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ca4e-107">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca4e-108">Тип: **[ **LPSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ca4e-108">Type: **[**LPSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ca4e-109">Адрес указателя для получения имени этого файлового объекта данных.</span><span class="sxs-lookup"><span data-stu-id="3ca4e-109">Address of a pointer to receive the name of this file data object.</span></span> <span data-ttu-id="3ca4e-110">Если этот параметр имеет **значение NULL**, пуисизе будет возвращать размер строки.</span><span class="sxs-lookup"><span data-stu-id="3ca4e-110">If this parameter is **NULL**, then puiSize will return the size of the string.</span></span> <span data-ttu-id="3ca4e-111">Если параметр szName указывает на допустимую память, имя этого файлового объекта данных будет скопировано в объект szName до количества символов, заданного параметром Пуисизе.</span><span class="sxs-lookup"><span data-stu-id="3ca4e-111">If szName points to valid memory, the name of this file data object will be copied into szName up to the number of characters given by puiSize.</span></span>

</dd> <dt>

<span data-ttu-id="3ca4e-112">*пуисизе* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="3ca4e-112">*puiSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca4e-113">Type: **[ **size \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3ca4e-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3ca4e-114">Указатель на размер строки, представляющей имя этого объекта файловых данных.</span><span class="sxs-lookup"><span data-stu-id="3ca4e-114">Pointer to the size of the string that represents the name of this file data object.</span></span> <span data-ttu-id="3ca4e-115">Этот параметр может иметь **значение NULL** , если szName предоставляет ссылку на имя.</span><span class="sxs-lookup"><span data-stu-id="3ca4e-115">This parameter can be **NULL** if szName provides a reference to the name.</span></span> <span data-ttu-id="3ca4e-116">Этот параметр возвращает размер строки, если параметр szName имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3ca4e-116">This parameter will return the size of the string if szName is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ca4e-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ca4e-117">Return value</span></span>

<span data-ttu-id="3ca4e-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3ca4e-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3ca4e-119">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="3ca4e-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3ca4e-120">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="3ca4e-120">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ca4e-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ca4e-121">Remarks</span></span>

<span data-ttu-id="3ca4e-122">Чтобы этот метод был выполнен, параметр szName или *пуисизе* должен иметь значение, отличное от **null**.</span><span class="sxs-lookup"><span data-stu-id="3ca4e-122">For this method to succeed, either szName or *puiSize* must be non-**NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ca4e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="3ca4e-123">Requirements</span></span>



| <span data-ttu-id="3ca4e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="3ca4e-124">Requirement</span></span> | <span data-ttu-id="3ca4e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="3ca4e-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca4e-126">Header</span><span class="sxs-lookup"><span data-stu-id="3ca4e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3ca4e-127"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ca4e-127"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="3ca4e-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3ca4e-128">Library</span></span><br/> | <dl> <span data-ttu-id="3ca4e-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ca4e-129"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3ca4e-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ca4e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ca4e-131">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="3ca4e-131">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
