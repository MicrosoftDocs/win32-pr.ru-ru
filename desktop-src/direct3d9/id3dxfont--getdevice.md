---
description: Извлекает устройство Direct3D, связанное с объектом Font.
ms.assetid: c713cbe2-6e6e-476b-a995-14fa149cb088
title: Метод ID3DXFont::-Device (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2de1b6e2c3b2c2b61576c739d96abc8b8fc8851a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355853"
---
# <a name="id3dxfontgetdevice-method"></a><span data-ttu-id="d3255-103">Метод ID3DXFont:: of Device</span><span class="sxs-lookup"><span data-stu-id="d3255-103">ID3DXFont::GetDevice method</span></span>

<span data-ttu-id="d3255-104">Извлекает устройство Direct3D, связанное с объектом Font.</span><span class="sxs-lookup"><span data-stu-id="d3255-104">Retrieves the Direct3D device associated with the font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3255-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3255-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="d3255-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3255-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3255-107">*ппдевице* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d3255-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3255-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="d3255-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="d3255-109">Адрес указателя на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий объект устройства Direct3D, связанный с объектом Font.</span><span class="sxs-lookup"><span data-stu-id="d3255-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3255-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3255-110">Return value</span></span>

<span data-ttu-id="d3255-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d3255-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d3255-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="d3255-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d3255-113">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="d3255-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3255-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3255-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d3255-115">Вызов этого метода приведет к увеличению внутреннего счетчика ссылок в интерфейсе [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="d3255-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="d3255-116">Не забудьте вызвать [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , когда вы завершите работу с этим интерфейсом **IDirect3DDevice9** , или у вас будет утечка памяти.</span><span class="sxs-lookup"><span data-stu-id="d3255-116">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d3255-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d3255-117">Requirements</span></span>



| <span data-ttu-id="d3255-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d3255-118">Requirement</span></span> | <span data-ttu-id="d3255-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d3255-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3255-120">Header</span><span class="sxs-lookup"><span data-stu-id="d3255-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d3255-121"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3255-121"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d3255-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d3255-122">Library</span></span><br/> | <dl> <span data-ttu-id="d3255-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3255-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d3255-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3255-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3255-125">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="d3255-125">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
