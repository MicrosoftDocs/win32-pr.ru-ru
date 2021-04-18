---
description: Регистрирует пользовательские шаблоны.
ms.assetid: e142a0f2-d0ef-4479-82cd-ba8d5059d1d2
title: 'Метод ID3DXFile:: Регистертемплатес (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7864b63d55ba219c5076920acc809f824bc1820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713778"
---
# <a name="id3dxfileregistertemplates-method"></a><span data-ttu-id="f6cdc-103">Метод ID3DXFile:: Регистертемплатес</span><span class="sxs-lookup"><span data-stu-id="f6cdc-103">ID3DXFile::RegisterTemplates method</span></span>

<span data-ttu-id="f6cdc-104">Регистрирует пользовательские шаблоны.</span><span class="sxs-lookup"><span data-stu-id="f6cdc-104">Registers custom templates.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6cdc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6cdc-105">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPCVOID pvData,
  [in] SIZE_T  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="f6cdc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6cdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6cdc-107">*пвдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6cdc-107">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6cdc-108">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6cdc-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f6cdc-109">Указатель на буфер, состоящий из файла. x в текстовом или двоичном формате, содержащем шаблоны.</span><span class="sxs-lookup"><span data-stu-id="f6cdc-109">Pointer to a buffer consisting of a .x file in text or binary format that contains templates.</span></span>

</dd> <dt>

<span data-ttu-id="f6cdc-110">*кбсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6cdc-110">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6cdc-111">Type: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6cdc-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f6cdc-112">Размер буфера, на который указывает Пвдата, в байтах.</span><span class="sxs-lookup"><span data-stu-id="f6cdc-112">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6cdc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6cdc-113">Return value</span></span>

<span data-ttu-id="f6cdc-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f6cdc-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f6cdc-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="f6cdc-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f6cdc-116">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадвалуе, D3DXFERR \_ парсиррор.</span><span class="sxs-lookup"><span data-stu-id="f6cdc-116">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6cdc-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6cdc-117">Remarks</span></span>

<span data-ttu-id="f6cdc-118">В следующем фрагменте кода приведен пример вызова **регистертемплатес** и пример содержимого для буфера, на который указывает **пвдата** .</span><span class="sxs-lookup"><span data-stu-id="f6cdc-118">The following code fragment provides an example call to **RegisterTemplates** And example contents for the buffer to which **pvData** points.</span></span>


```
#define XSKINEXP_TEMPLATES \
    "xof 0303txt 0032\
    template XSkinMeshHeader \
    { \
        <3CF169CE-FF7C-44ab-93C0-F78F62D172E2> \
        WORD nMaxSkinWeightsPerVertex; \
        WORD nMaxSkinWeightsPerFace; \
        WORD nBones; \
    } \
    template VertexDuplicationIndices \
    { \
        <B8D65549-D7C9-4995-89CF-53A9A8B031E3> \
        DWORD nIndices; \
        DWORD nOriginalVertices; \
        array DWORD indices[nIndices]; \
    } \
    template SkinWeights \
    { \
        <6F0D123B-BAD2-4167-A0D0-80224F25FABB> \
        STRING transformNodeName;\
        DWORD nWeights; \
        array DWORD vertexIndices[nWeights]; \
        array float weights[nWeights]; \
        Matrix4x4 matrixOffset; \
    }"
.
.
.
        
LPD3DXFILE pD3DXFile = NULL;

if ( FAILED 
        (hr = pD3DXFile->RegisterTemplates( 
            (LPVOID)XSKINEXP_TEMPLATES,
            sizeof( XSKINEXP_TEMPLATES ) - 1 ) ) )
goto End;
```



<span data-ttu-id="f6cdc-119">Все шаблоны должны указывать имя и UUID.</span><span class="sxs-lookup"><span data-stu-id="f6cdc-119">All templates must specify a name and a UUID.</span></span>

<span data-ttu-id="f6cdc-120">Этот метод вызывает метод [**регистеренумтемплатес**](id3dxfile--registerenumtemplates.md) , получая указатель интерфейса [**ID3DXFileEnumObject**](id3dxfileenumobject.md) , вызывая [**креатинумобжект**](id3dxfile--createenumobject.md) с **пвдата** в качестве первого параметра.</span><span class="sxs-lookup"><span data-stu-id="f6cdc-120">This method calls the [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) method, obtaining an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) interface pointer by calling [**CreateEnumObject**](id3dxfile--createenumobject.md) with **pvData** as the first parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6cdc-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f6cdc-121">Requirements</span></span>



| <span data-ttu-id="f6cdc-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f6cdc-122">Requirement</span></span> | <span data-ttu-id="f6cdc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f6cdc-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6cdc-124">Header</span><span class="sxs-lookup"><span data-stu-id="f6cdc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f6cdc-125"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6cdc-125"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="f6cdc-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f6cdc-126">Library</span></span><br/> | <dl> <span data-ttu-id="f6cdc-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6cdc-127"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f6cdc-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6cdc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6cdc-129">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="f6cdc-129">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="f6cdc-130">**регистеренумтемплатес**</span><span class="sxs-lookup"><span data-stu-id="f6cdc-130">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md)
</dt> </dl>

 

 
