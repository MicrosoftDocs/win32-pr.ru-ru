---
description: Регистрирует пользовательские шаблоны при наличии объекта перечисления ID3DXFileEnumObject.
ms.assetid: 1b0c71db-639b-4836-8a65-7d0a2ed3ba4f
title: 'Метод ID3DXFile:: Регистеренумтемплатес (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterEnumTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 89a8b136bdc0e202fc87ba8fd4d7f013203814eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424446"
---
# <a name="id3dxfileregisterenumtemplates-method"></a><span data-ttu-id="a79e6-103">Метод ID3DXFile:: Регистеренумтемплатес</span><span class="sxs-lookup"><span data-stu-id="a79e6-103">ID3DXFile::RegisterEnumTemplates method</span></span>

<span data-ttu-id="a79e6-104">Регистрирует пользовательские шаблоны при наличии объекта перечисления [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="a79e6-104">Registers custom templates, given an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a79e6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a79e6-105">Syntax</span></span>


```C++
HRESULT RegisterEnumTemplates(
  [in] ID3DXFileEnumObject *pEnum
);
```



## <a name="parameters"></a><span data-ttu-id="a79e6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a79e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a79e6-107">*пенум* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a79e6-107">*pEnum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a79e6-108">Тип: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="a79e6-108">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\***</span></span>

<span data-ttu-id="a79e6-109">Указатель на объект перечисления [**ID3DXFileEnumObject**](id3dxfileenumobject.md) , содержащий шаблоны.</span><span class="sxs-lookup"><span data-stu-id="a79e6-109">Pointer to an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object that contains templates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a79e6-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a79e6-110">Return value</span></span>

<span data-ttu-id="a79e6-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a79e6-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a79e6-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="a79e6-112">If the method succeeds, the return value is S\_OK .</span></span>

<span data-ttu-id="a79e6-113">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="a79e6-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="a79e6-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a79e6-114">Remarks</span></span>

<span data-ttu-id="a79e6-115">При вызове этого метода он копирует шаблоны, хранящиеся в ID3DXFileEnumObject, представляющие файл, в локальное хранилище шаблонов объекта [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="a79e6-115">When this method is called, it copies templates stored with the ID3DXFileEnumObject, representing the file, to the local template store of the [**ID3DXFile**](id3dxfile.md) object.</span></span>

<span data-ttu-id="a79e6-116">Если указатель [**ID3DXFileEnumObject**](id3dxfileenumobject.md) недоступен, вызовите вместо этого метод [**регистертемплатес**](id3dxfile--registertemplates.md) .</span><span class="sxs-lookup"><span data-stu-id="a79e6-116">If an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) pointer is not available, call the [**RegisterTemplates**](id3dxfile--registertemplates.md) method instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="a79e6-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a79e6-117">Requirements</span></span>



| <span data-ttu-id="a79e6-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a79e6-118">Requirement</span></span> | <span data-ttu-id="a79e6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a79e6-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a79e6-120">Header</span><span class="sxs-lookup"><span data-stu-id="a79e6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a79e6-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="a79e6-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="a79e6-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a79e6-122">Library</span></span><br/> | <dl> <span data-ttu-id="a79e6-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a79e6-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a79e6-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a79e6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a79e6-125">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="a79e6-125">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="a79e6-126">**регистертемплатес**</span><span class="sxs-lookup"><span data-stu-id="a79e6-126">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




