---
description: Запрашивает в ранее созданное представление в режиме ядра объекта Microsoft DirectDraw для его возможностей.
ms.assetid: ec07c7ef-4c57-4ed9-849b-f30692cc3181
title: Функция Нтгдиддкуеридиректдравобжект (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdQueryDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 2cd87bc1cc278f8ee680dbd458ed3b92cc699a060021a91535de66996376db84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103824"
---
# <a name="ntgdiddquerydirectdrawobject-function"></a>Функция Нтгдиддкуеридиректдравобжект

\[Эта функция может быть изменена при каждой редакции операционной системы. Вместо этого используйте DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]

Запрашивает в ранее созданное представление в режиме ядра объекта Microsoft DirectDraw для его возможностей.

## <a name="syntax"></a>Синтаксис


```C++
BOOL APIENTRY NtGdiDdQueryDirectDrawObject(
  _In_  HANDLE                      hDirectDrawLocal,
  _Out_ DD_HALINFO                  *pHalInfo,
        DWORD                       *pCallBackFlags,
  _Out_ LPD3DNTHAL_CALLBACKS        puD3dCallbacks,
  _Out_ LPD3DNTHAL_GLOBALDRIVERDATA puD3dDriverData,
  _Out_ PDD_D3DBUFCALLBACKS         puD3dBufferCallbacks,
  _Out_ LPDDSURFACEDESC             puD3dTextureFormats,
  _Out_ DWORD                       *puNumHeaps,
  _Out_ VIDEOMEMORY                 *puvmList,
  _Out_ DWORD                       *puNumFourCC,
  _Out_ DWORD                       *puFourCC
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдиректдравлокал* \[ окне\]
</dt> <dd>

Обработано ранее созданное устройство DirectDraw режима ядра.

</dd> <dt>

*фалинфо* \[ заполняет\]
</dt> <dd>

Указатель на структуру [**DD \_ халинфо**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) , которая будет заполнена возможностями устройства. Дополнительные сведения см. в документации по DDK.

</dd> <dt>

*пкаллбаккфлагс* 
</dt> <dd>

Указатель на предоставленный вызывающим объектом буфер, в котором хранятся флаги обратного вызова, переданные драйвером. Буфер должен иметь размер 3 \* sizeof (DWORD) и сохраняет флаги обратного вызова в следующем порядке: пкаллбаккфлагс \[ 0 \] для флагов в параметрах [**\_ обратного вызова DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks), Пкаллбаккфлагс \[ 1 \] для флагов в [**DD \_ сурфацекаллбаккс**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks)и пкаллбаккфлагс \[ 2 \] для флагов в [**DD \_ палеттекаллбаккс**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks). Дополнительные сведения см. в документации по DDK.

</dd> <dt>

*puD3dCallbacks* \[ заполняет\]
</dt> <dd>

Указатель на таблицу указателей обратного вызова Direct3D. Таблица заполняется указателями на функции в Gdi32.dll, имитирующие драйвер экрана Direct3D. Эта таблица обратного вызова идентична \_ структуре D3DHAL D3DCALLBACKS, обсуждаемой в документации по DDK.

</dd> <dt>

*puD3dDriverData* \[ заполняет\]
</dt> <dd>

Указатель на [**данные \_ глобалдривердата D3DHAL**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) , как описано в документации по DDK.

</dd> <dt>

*puD3dBufferCallbacks* \[ заполняет\]
</dt> <dd>

Указатель на таблицу указателей обратного вызова. Таблица заполняется указателями на функции в Gdi32.dll, имитирующие драйвер экрана Direct3D. Эта таблица обратного вызова идентична \_ структуре ддхал ддексебуфкаллбаккс, которая сопоставляется с структурой [**\_ D3DBUFCALLBACKS DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) , обсуждаемой в документации по DDK, за исключением того, что члены XxxD3DBuffer в **DD \_ D3DBUFCALLBACKS** заменяются ксксксексекутебуффер в ддхал \_ ддексебуфкаллбаккс.

</dd> <dt>

*puD3dTextureFormats* \[ заполняет\]
</dt> <dd>

Указатель на массив структур [**ддсурфацедеск**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) , определяющих набор допустимых форматов текстуры.

</dd> <dt>

*пунумхеапс* \[ заполняет\]
</dt> <dd>

Указатель на элемент **двнумхеапс** в [**DD \_ халинфо**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**Вмидата**. Член **двнумхеапс** указывает количество куч памяти в *пувмлист*. Дополнительные сведения см. в документации по DDK.

</dd> <dt>

*пувмлист* \[ заполняет\]
</dt> <dd>

Указатель на список дескрипторов кучи видеопамяти. Может иметь **значение NULL**. Этот параметр не используется, так как управление видеопамятью полностью обрабатывается в режиме ядра.

</dd> <dt>

*пунумфауркк* \[ заполняет\]
</dt> <dd>

Указатель на элемент **пунумфауркккодес** в [**DD \_ халинфо**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**Ддкапс**. Элемент **пунумфауркккодес** указывает количество кодов с [четырьмя символами (FOURCC)](../directshow/fourcc-codes.md) , поддерживаемых драйвером. Дополнительные сведения см. в документации по DDK.

</dd> <dt>

*пуфауркк* \[ заполняет\]
</dt> <dd>

Указатель на список поддерживаемых форматов поверхностей [с четырьмя символами (FOURCC)](../directshow/fourcc-codes.md) . Может иметь **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха эта функция возвращает **значение true**. в противном случае возвращается **значение false**.

## <a name="remarks"></a>Remarks

Вызов этой функции предназначен для выполнения в два этапа. На первом шаге *пуфауркк*, *пувмлист* и *puD3dTextureFormats* должны иметь **значение NULL**, а [**ддкуеридиректдравобжект**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) будет заполнять [**DD \_ халинфо**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**Ддкапс**. **двнумфауркккодес**, **DD \_ халинфо**.**Вмидата**. **двнумхеапс** и [**D3DHAL \_ глобалдривердата**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**Двнумтекстуреформатс** с числом возвращаемых записей. Во втором вызове вызывающий объект должен выделить массивы указанного размера и передать эти указатели вместо значений **null** в параметрах *пуфауркк*, *пувмлист* и *puD3dTextureFormats* . После этого массивы будут заполнены соответствующими данными.

В приложениях рекомендуется использовать интерфейсы API DirectDraw и [Direct3D](../direct3d10/d3d10-graphics-reference.md) для создания объектов графических устройств и управления ими. Эти конструкции являются абстрактным процессом создания устройств в упрощенном и независимом от операционной системе виде.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Нтгди. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Поддержка клиентов низкого уровня графики](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**ддкуеридиректдравобжект**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject)
</dt> <dt>

[**нтгдиддкреатедиректдравобжект**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> </dl>

 

 
