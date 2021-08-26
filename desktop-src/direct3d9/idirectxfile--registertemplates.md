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
ms.openlocfilehash: 685e97ec28241348ff4a969c444b6da5638aeba01af8be35cc5490a0d2be0a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846964"
---
# <a name="idirectxfileregistertemplates-method"></a>Метод Идиректксфиле:: Регистертемплатес

Регистрирует пользовательские шаблоны. Не рекомендуется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RegisterTemplates(
  [in] LPVOID pvData,
  [in] DWORD  cbSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвдата* \[ окне\]
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**

Указатель на буфер, состоящий из файла DirectX в текстовом или двоичном формате, который содержит шаблоны.

</dd> <dt>

*кбсизе* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Размер буфера, на который указывает Пвдата, в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК. Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадфилефлоатсизе, дксфилирр \_ БАДФИЛЕТИПЕ, дксфилирр \_ бадфилеверсион, ДКСФИЛИРР \_ BADVALUE, DXFILEERR \_ PARSEERROR.

## <a name="remarks"></a>Remarks

В следующем фрагменте кода приведен пример вызова **регистертемплатес** и пример содержимого для буфера, на который указывает пвдата.


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



Все шаблоны должны указывать имя и универсальный уникальный идентификатор (UUID).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[идиректксфиле](idirectxfile.md)
</dt> </dl>

 

 
