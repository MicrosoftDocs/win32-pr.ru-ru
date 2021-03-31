---
description: Методы, используемые для работы с файлами DirectX. x, могут возвращать следующие значения в дополнение к стандартным возвращаемым значениям COM.
ms.assetid: b1d04fab-25cb-431d-942e-74092bc9c5c2
title: Возвращаемые значения D3DXFERR (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFERR
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: cab1cc5e70b6204c832fd9fe5b0fecac4276f578
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157190"
---
# <a name="d3dxferr-return-values"></a>Возвращаемые значения D3DXFERR

Методы, используемые для работы с файлами DirectX. x, могут возвращать следующие значения в дополнение к стандартным возвращаемым значениям COM.

<dl> <dt>

<span id="D3DXFERR_BADARRAYSIZE"></span><span id="d3dxferr_badarraysize"></span>**D3DXFERR \_ бадаррайсизе**
</dt> <dd>

Массив превышает допустимый размер.

</dd> <dt>

<span id="D3DXFERR_BADCACHEFILE"></span><span id="d3dxferr_badcachefile"></span>**D3DXFERR \_ бадкачефиле**
</dt> <dd>

Не удалось прочитать файл кэша.

</dd> <dt>

<span id="D3DXFERR_BADDataReference"></span><span id="d3dxferr_baddatareference"></span><span id="D3DXFERR_BADDATAREFERENCE"></span>**D3DXFERR \_ баддатареференце**
</dt> <dd>

Не удалось получить данные элемента шаблона.

</dd> <dt>

<span id="D3DXFERR_BADFILE"></span><span id="d3dxferr_badfile"></span>**D3DXFERR \_ бадфиле**
</dt> <dd>

Не удалось выполнить операцию чтения или записи файла.

</dd> <dt>

<span id="D3DXFERR_BADFILEFLOATSIZE"></span><span id="d3dxferr_badfilefloatsize"></span>**D3DXFERR \_ бадфилефлоатсизе**
</dt> <dd>

Размер файла не соответствует ожидаемому размеру.

</dd> <dt>

<span id="D3DXFERR_BADFILETYPE"></span><span id="d3dxferr_badfiletype"></span>**D3DXFERR \_ бадфилетипе**
</dt> <dd>

Файл имеет недопустимый формат.

</dd> <dt>

<span id="D3DXFERR_BADFILEVERSION"></span><span id="d3dxferr_badfileversion"></span>**D3DXFERR \_ бадфилеверсион**
</dt> <dd>

Файл имеет недопустимую версию формата.

</dd> <dt>

<span id="D3DXFERR_BADOBJECT"></span><span id="d3dxferr_badobject"></span>**D3DXFERR \_ бадобжект**
</dt> <dd>

Не удалось выполнить чтение или запись данных в объект.

</dd> <dt>

<span id="D3DXFERR_BADRESOURCE"></span><span id="d3dxferr_badresource"></span>**D3DXFERR \_ бадресаурце**
</dt> <dd>

Сбой операции с ресурсом.

</dd> <dt>

<span id="D3DXFERR_BADTYPE"></span><span id="d3dxferr_badtype"></span>**D3DXFERR \_ бадтипе**
</dt> <dd>

Файл не соответствует известным типам шаблонов.

</dd> <dt>

<span id="D3DXFERR_BADVALUE"></span><span id="d3dxferr_badvalue"></span>**D3DXFERR \_ бадвалуе**
</dt> <dd>

Переменная находится за пределами ожидаемого диапазона; обычно возвращается, если указатель на объект является недопустимым.

</dd> <dt>

<span id="D3DXFERR_FILENOTFOUND"></span><span id="d3dxferr_filenotfound"></span>**D3DXFERR \_ FILENOTFOUND**
</dt> <dd>

Не удалось найти допустимый маркер для указанного файла.

</dd> <dt>

<span id="D3DXFERR_NOMOREDATA"></span><span id="d3dxferr_nomoredata"></span>**D3DXFERR \_ номоредата**
</dt> <dd>

Смещение указателя, развернутое за концом буфера.

</dd> <dt>

<span id="D3DXFERR_NOMOREOBJECTS"></span><span id="d3dxferr_nomoreobjects"></span>**D3DXFERR \_ номореобжектс**
</dt> <dd>

Больше нет доступных дочерних объектов.

</dd> <dt>

<span id="D3DXFERR_NOTDONEYET"></span><span id="d3dxferr_notdoneyet"></span>**D3DXFERR \_ нотдонэйет**
</dt> <dd>

Тип данных не соответствует допустимым типам.

</dd> <dt>

<span id="D3DXFERR_NOTFOUND"></span><span id="d3dxferr_notfound"></span>**D3DXFERR \_ NotFound**
</dt> <dd>

Не удалось найти объект по указанным параметрам.

</dd> <dt>

<span id="D3DXFERR_PARSEERROR"></span><span id="d3dxferr_parseerror"></span>**D3DXFERR \_ парсиррор**
</dt> <dd>

Не удалось проанализировать поток данных.

</dd> <dt>

<span id="D3DXFERR_RESOURCENOTFOUND"></span><span id="d3dxferr_resourcenotfound"></span>**D3DXFERR \_ RESOURCENOTFOUND**
</dt> <dd>

Не удалось найти допустимый маркер для указанного ресурса.

</dd> </dl>

## <a name="remarks"></a>Комментарии

\_Для создания кодов ошибок используется FACD3DXF код механизма ошибок в файле x. Пример:


```
#define _FACD3DXF           0x876
#define D3DXFERR_BADOBJECT  MAKE_HRESULT( 1, _FACD3DXF, 900 )
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9xof. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы файла D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> </dl>

 

 




