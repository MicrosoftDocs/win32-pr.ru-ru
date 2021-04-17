---
description: Создает файл. x и сохраняет иерархию сетки и соответствующие анимации в ней.
ms.assetid: 803926fe-8cb7-422a-9920-56f7d0b0d0ea
title: Функция D3DXSaveMeshHierarchyToFile (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshHierarchyToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2de65f9bc2f9e40a5bc07c6f0b4d00112f0df21
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694136"
---
# <a name="d3dxsavemeshhierarchytofile-function"></a>Функция D3DXSaveMeshHierarchyToFile

Создает файл. x и сохраняет иерархию сетки и соответствующие анимации в ней.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXSaveMeshHierarchyToFile(
  _In_       LPCSTR                    pFilename,
  _In_       DWORD                     XFormat,
  _In_ const D3DXFRAME                 *pFrameRoot,
  _In_       LPD3DXANIMATIONCONTROLLER pAnimController,
  _In_       LPD3DXSAVEUSERDATA        pUserDataSaver
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфиленаме* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Указатель на строку, указывающую имя файла x, определяющего сохраненную сетку. Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае строковый тип данных разрешается в LPCSTR. См. заметки.

</dd> <dt>

*Ксформат* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Формат файла. x (Text или binary, сжатый или не). См. раздел D3DXF \_ FILEFORMAT. \_Сжатый D3DXF FILEFORMAT \_ можно объединить (с помощью логического или) с \_ \_ флагами текста D3DXF FILEFORMAT binary или D3DXF \_ FILEFORMAT, \_ чтобы уменьшить размер выходного файла.

</dd> <dt>

*пфрамерут* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXFRAME**](d3dxframe.md) \***

Корневой узел для сохраняемой иерархии. См. [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*панимконтроллер* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**

Контроллер анимации, на котором хранятся наборы анимации. См. [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> <dt>

*пусердатасавер* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**

Предоставляемый приложением интерфейс, позволяющий сохранять данные пользователя. См. [**ID3DXSaveUserData**](id3dxsaveuserdata.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в D3DXSaveMeshHierarchyToFileW. В противном случае вызов функции разрешается в D3DXSaveMeshHierarchyToFileA.

Эта функция не сохраняет сжатые наборы анимации.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции анимации](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> <dt>

[Ссылка на X файл](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 
