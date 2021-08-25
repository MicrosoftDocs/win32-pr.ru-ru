---
description: Возвращает сведения о сжатых буферах, необходимых для декодирования с аппаратным ускорением.
ms.assetid: 5a9fb077-fd79-4faa-a0f8-b3ac987adf36
title: 'Метод IDirect3DVideoDevice9:: Жетдксвакомпресседбуфферинфо (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVACompressedBufferInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: efb96ec457cdb81f89982947bf1b9bc40543789b2e9ac253d83c81727f1efae5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942294"
---
# <a name="idirect3dvideodevice9getdxvacompressedbufferinfo-method"></a>Метод IDirect3DVideoDevice9:: Жетдксвакомпресседбуфферинфо

Возвращает сведения о сжатых буферах, необходимых для декодирования с аппаратным ускорением.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDXVACompressedBufferInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pNumBuffers,
   DXVACompBufferInfo *pBufferInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пгуид* 
</dt> <dd>

Указатель на идентификатор GUID, указывающий профиль ДКСВА. Чтобы получить список поддерживаемых профилей, вызовите [**IDirect3DVideoDevice9:: жетдксвагуидс**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*пункомпдата* 
</dt> <dd>

Указатель на структуру [**дксваункомпдатаинфо**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) , указывающую размер и формат пикселей для несжатых данных.

</dd> <dt>

*пнумбуфферс* 
</dt> <dd>

В поле входные данные указывает количество элементов в массиве *пбуфферинфо* . Если *пбуфферинфо* имеет **значение NULL**, значение `*pNumBuffers` должно быть равно нулю.

В выходных данных, если *пбуфферинфо* имеет **значение NULL**, *пнумбуфферс* получает размер массива для выделения. В противном случае *пнумбуфферс* получает фактическое число элементов, копируемых в массив *пбуфферинфо* .

</dd> <dt>

*пбуфферинфо* 
</dt> <dd>

Адрес массива структур [**дксвакомпбуфферинфо**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) или **значение NULL**. Если значение не равно **null**, метод копирует список структур **дксвакомпбуфферинфо** в этот массив. Каждая структура соответствует одному типу сжатого буфера данных, который используется ускорителем видео.

Перед вызовом этого метода установите все элементы массива в ноль.

Каждый индекс массива соответствует одному из типов ДКСВА Surface, определенных в дксва. h. Видеоускоритель возвращает список, в котором **дксва число числовых \_ \_ типов в \_ \_ буфере Comp** . Дополнительные сведения см. в [спецификации дксва 1,0](/windows-hardware/drivers/display/directx-video-acceleration), раздел 3,4, "список описания буферов". Если определенный тип буфера не используется профилем ДКСВА, запись в этом индексе будет содержать нули для всех значений.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                    |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                              |
| Заголовок<br/>                   | <dl> <dt>Дксва. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 
