---
description: Создает объект Save, который будет использоваться для сохранения данных в файл. x.
ms.assetid: da064e83-605f-4c86-985d-9a0961c18e01
title: 'Метод ID3DXFile:: Креатесавеобжект (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d7c5b3de020ad50abfd8834aabbdc8e6e848d71d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713805"
---
# <a name="id3dxfilecreatesaveobject-method"></a><span data-ttu-id="e0899-103">Метод ID3DXFile:: Креатесавеобжект</span><span class="sxs-lookup"><span data-stu-id="e0899-103">ID3DXFile::CreateSaveObject method</span></span>

<span data-ttu-id="e0899-104">Создает объект Save, который будет использоваться для сохранения данных в файл. x.</span><span class="sxs-lookup"><span data-stu-id="e0899-104">Creates a save object that will be used to save data to a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0899-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0899-105">Syntax</span></span>


```C++
HRESULT CreateSaveObject(
  [in]  LPCVOID               pData,
  [in]  D3DXF_FILESAVEOPTIONS flags,
  [in]  D3DXF_FILEFORMAT      dwFileFormat,
  [out] ID3DXFileSaveObject   **ppSaveObj
);
```



## <a name="parameters"></a><span data-ttu-id="e0899-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0899-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0899-107">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0899-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0899-108">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0899-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0899-109">Указатель на имя файла, используемого для сохранения данных.</span><span class="sxs-lookup"><span data-stu-id="e0899-109">Pointer to the name of the file to use for saving data.</span></span>

</dd> <dt>

<span data-ttu-id="e0899-110">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0899-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0899-111">Тип: **[D3DXF \_ филесавеоптионс](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="e0899-111">Type: **[D3DXF\_FILESAVEOPTIONS](d3dxf.md)**</span></span>

<span data-ttu-id="e0899-112">Значение типа, указывающее имя файла, в который должны быть сохранены данные.</span><span class="sxs-lookup"><span data-stu-id="e0899-112">Value that specifies the name of the file to which data is to be saved.</span></span> <span data-ttu-id="e0899-113">Это значение может быть одним из флагов [параметров сохранения файла](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="e0899-113">This value can be one of the [File Save Options](d3dxf.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="e0899-114">*двфилеформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0899-114">*dwFileFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0899-115">Тип: **[D3DXF \_ FILEFORMAT](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="e0899-115">Type: **[D3DXF\_FILEFORMAT](d3dxf.md)**</span></span>

<span data-ttu-id="e0899-116">Указывает формат, используемый при сохранении файла. x.</span><span class="sxs-lookup"><span data-stu-id="e0899-116">Indicates the format to use when saving the .x file.</span></span> <span data-ttu-id="e0899-117">Это значение может быть одним из флагов [формата файла](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="e0899-117">This value can be one of the [File Formats](d3dxf.md) flags.</span></span> <span data-ttu-id="e0899-118">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="e0899-118">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e0899-119">*ппсавеобж* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e0899-119">*ppSaveObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0899-120">Тип: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e0899-120">Type: **[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span></span>

<span data-ttu-id="e0899-121">Адрес указателя на интерфейс [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) , представляющий созданный объект Save.</span><span class="sxs-lookup"><span data-stu-id="e0899-121">Address of a pointer to an [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface, representing the created save object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0899-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0899-122">Return value</span></span>

<span data-ttu-id="e0899-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0899-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0899-124">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="e0899-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e0899-125">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадвалуе, D3DXFERR \_ парсиррор.</span><span class="sxs-lookup"><span data-stu-id="e0899-125">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0899-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0899-126">Remarks</span></span>

<span data-ttu-id="e0899-127">После использования этого метода используйте методы интерфейса [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) для создания объектов данных и сохранения шаблонов или данных.</span><span class="sxs-lookup"><span data-stu-id="e0899-127">After using this method, use methods of the [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface to create data objects and to save templates or data.</span></span>

<span data-ttu-id="e0899-128">Для сохраненного формата файла *двфилеформат* необходимо указать один из двоичных, устаревших двоичных или текстовых флагов в [форматах файлов](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="e0899-128">For the saved file format *dwFileFormat*, one of the binary, legacy binary, or text flags in [File Formats](d3dxf.md) must be specified.</span></span> <span data-ttu-id="e0899-129">Файл можно сжать с помощью необязательного \_ \_ флага сжатия D3DXF FILEFORMAT.</span><span class="sxs-lookup"><span data-stu-id="e0899-129">The file can be compressed by using the optional D3DXF\_FILEFORMAT\_COMPRESSED flag.</span></span>

<span data-ttu-id="e0899-130">Значения формата файла можно комбинировать в логическом или для создания сжатого текста или сжатых двоичных файлов.</span><span class="sxs-lookup"><span data-stu-id="e0899-130">The file format values can be combined in a logical OR to create compressed text or compressed binary files.</span></span> <span data-ttu-id="e0899-131">Если указать, что формат файла должен быть текстовым и сжатым, файл будет записан первым в виде текста, а затем сжат.</span><span class="sxs-lookup"><span data-stu-id="e0899-131">If you indicate that the file format should be text and compressed, the file will be written out first as text and then compressed.</span></span> <span data-ttu-id="e0899-132">Однако сжатые текстовые файлы не так эффективны, как двоичные текстовые файлы; в большинстве случаев необходимо указать двоичные и сжатые данные.</span><span class="sxs-lookup"><span data-stu-id="e0899-132">However, compressed text files are not as efficient as binary text files; in most cases, therefore, you will want to indicate binary and compressed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0899-133">Требования</span><span class="sxs-lookup"><span data-stu-id="e0899-133">Requirements</span></span>



| <span data-ttu-id="e0899-134">Требование</span><span class="sxs-lookup"><span data-stu-id="e0899-134">Requirement</span></span> | <span data-ttu-id="e0899-135">Значение</span><span class="sxs-lookup"><span data-stu-id="e0899-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0899-136">Header</span><span class="sxs-lookup"><span data-stu-id="e0899-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e0899-137"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0899-137"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="e0899-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e0899-138">Library</span></span><br/> | <dl> <span data-ttu-id="e0899-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0899-139"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e0899-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0899-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0899-141">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="e0899-141">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="e0899-142">**ID3DXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="e0899-142">**ID3DXFileSaveObject**</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 
