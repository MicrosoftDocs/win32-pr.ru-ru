---
description: Регистрирует пользовательские шаблоны. Не рекомендуется.
ms.assetid: f9b24800-83a5-45bf-b19f-b247c88a2c2c
title: 'Метод Идиректксфиле:: Регистертемплатес (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 683a495398e7fe0718ee0642c7760b0a8590538c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664965"
---
# <a name="idirectxfileregistertemplates-method"></a><span data-ttu-id="81203-104">Метод Идиректксфиле:: Регистертемплатес</span><span class="sxs-lookup"><span data-stu-id="81203-104">IDirectXFile::RegisterTemplates method</span></span>

<span data-ttu-id="81203-105">Регистрирует пользовательские шаблоны.</span><span class="sxs-lookup"><span data-stu-id="81203-105">Registers custom templates.</span></span> <span data-ttu-id="81203-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="81203-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="81203-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81203-107">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPVOID pvData,
  [in] DWORD  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="81203-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="81203-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81203-109">*пвдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81203-109">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81203-110">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81203-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81203-111">Указатель на буфер, состоящий из файла DirectX в текстовом или двоичном формате, который содержит шаблоны.</span><span class="sxs-lookup"><span data-stu-id="81203-111">Pointer to a buffer consisting of a DirectX file in text or binary format that contains templates.</span></span>

</dd> <dt>

<span data-ttu-id="81203-112">*кбсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81203-112">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81203-113">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81203-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81203-114">Размер буфера, на который указывает Пвдата, в байтах.</span><span class="sxs-lookup"><span data-stu-id="81203-114">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81203-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81203-115">Return value</span></span>

<span data-ttu-id="81203-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="81203-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="81203-117">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="81203-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="81203-118">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадфилефлоатсизе, дксфилирр \_ БАДФИЛЕТИПЕ, дксфилирр \_ бадфилеверсион, ДКСФИЛИРР \_ BADVALUE, DXFILEERR \_ PARSEERROR.</span><span class="sxs-lookup"><span data-stu-id="81203-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADFILEFLOATSIZE, DXFILEERR\_BADFILETYPE, DXFILEERR\_BADFILEVERSION, DXFILEERR\_BADVALUE, DXFILEERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="81203-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81203-119">Remarks</span></span>

<span data-ttu-id="81203-120">В следующем фрагменте кода приведен пример вызова **регистертемплатес** и пример содержимого для буфера, на который указывает пвдата.</span><span class="sxs-lookup"><span data-stu-id="81203-120">The following code fragment provides an example call to **RegisterTemplates** And example contents for the buffer to which pvData points.</span></span>


```
    TIDirectXFile * pDXFile;
    char *szTemplates = "xof 0303txt 0032\
        template SimpleData { \
            <2b934580-9e9a-11cf-ab39-0020af71e433> \
            DWORD item1;DWORD item2;DWORD item3;} \
        template ArrayData { \
            <2b934581-9e9a-11cf-ab39-0020af71e433> \
            DWORD cItems; array DWORD aItem[2][cItems]; [...] } \
        template RestrictedData { \
            <2b934582-9e9a-11cf-ab39-0020af71e433> \
            DWORD item; [SimpleData]}";
    hr = pDXFile->RegisterTemplates(szTemplates, strlen(szTemplates));
    
    
```



<span data-ttu-id="81203-121">Все шаблоны должны указывать имя и универсальный уникальный идентификатор (UUID).</span><span class="sxs-lookup"><span data-stu-id="81203-121">All templates must specify a name and a Universally Unique Identifier (UUID).</span></span>

## <a name="requirements"></a><span data-ttu-id="81203-122">Требования</span><span class="sxs-lookup"><span data-stu-id="81203-122">Requirements</span></span>



| <span data-ttu-id="81203-123">Требование</span><span class="sxs-lookup"><span data-stu-id="81203-123">Requirement</span></span> | <span data-ttu-id="81203-124">Значение</span><span class="sxs-lookup"><span data-stu-id="81203-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81203-125">Header</span><span class="sxs-lookup"><span data-stu-id="81203-125">Header</span></span><br/>  | <dl> <span data-ttu-id="81203-126"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="81203-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="81203-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="81203-127">Library</span></span><br/> | <dl> <span data-ttu-id="81203-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81203-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81203-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81203-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81203-130">идиректксфиле</span><span class="sxs-lookup"><span data-stu-id="81203-130">IDirectXFile</span></span>](idirectxfile.md)
</dt> </dl>

 

 
