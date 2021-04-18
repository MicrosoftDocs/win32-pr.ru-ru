---
title: Метод Жетобжектдатаонклеарчаннел
description: Метод Жетобжектдатаонклеарчаннел передает блок данных объекта на открытый канал обратно в Windows Media диспетчер устройств.
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- Метод Жетобжектдатаонклеарчаннел Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- GetObjectDataOnClearChannel
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25b72df0dd27289153a97221fefbcb58f3a5ad13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694424"
---
# <a name="getobjectdataonclearchannel-method"></a>Метод Жетобжектдатаонклеарчаннел

Метод **жетобжектдатаонклеарчаннел** передает блок данных объекта на открытый канал обратно в Windows Media Диспетчер устройств.

Этот метод идентичен [**искпсекуриксчанже:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , за исключением того, что данные, возвращаемые этим методом, не шифруются. Поэтому этот метод является более эффективным.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetObjectDataOnClearChannel(
   IMDSPDevice *pDevice,
   BYTE        *pData,
   DWORD       *pdwSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* 
</dt> <dd>

Указатель на объект устройства.

</dd> <dt>

*pData* 
</dt> <dd>

Указатель на буфер для приема данных.

</dd> <dt>

*пдвсизе* 
</dt> <dd>

Указатель на **DWORD** , содержащий размер перемещения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение S \_ ОК. Если метод завершается с ошибкой, возвращается код ошибки **HRESULT** .



| Код возврата                                                                                                | Описание                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Проверка вмдм \_ E \_ Mac \_ не пройдена**</dt> </dl> | Недопустимый код проверки подлинности сообщения.<br/>                                    |
| <dl> <dt>**ВМДМ \_ E \_**</dt> </dl>           | Вызывающий объект не имеет прав, необходимых для выполнения запрошенной операции.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl>                    | Сбой метода. Прекращение взаимодействия с поставщиком содержимого.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Параметр является недопустимым указателем или **пустым** .<br/>                                   |
| <dl> <dt>**\_Ошибка E**</dt> </dl>                     | Произошла неизвестная ошибка.<br/>                                                   |



 

## <a name="remarks"></a>Комментарии

Для передачи данных Windows Media диспетчер устройств вызывает метод [трансферконтаинердатаонклеарчаннел](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) для получения данных контейнера. Затем вызывается **жетобжектдатаонклеарчаннел** для передачи блоков данных объекта от поставщика содержимого в Диспетчер устройств Windows Media. Если \_ параметр S ОК возвращается с *пдвсизе* , для которого установлено значение 0, Windows Media Диспетчер устройств не запрашивает никаких дополнительных данных.

Этот метод идентичен [**искпсекуриксчанже:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , за исключением того, что данные, возвращаемые этим методом, не шифруются. Поэтому этот метод является более эффективным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ВМСКП. idl</dt> </dl>    |
| Библиотека<br/> | <dl> <dt>Мссачлп. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Искпсекуриксчанже:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[**Интерфейс ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





