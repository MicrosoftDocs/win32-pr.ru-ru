---
description: В \_ константах линеопеноптион перечислены доступные параметры для открытия строки.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: Константы LINEOPENOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dee9182ff7a28627eebd695ce5d9c0877460b15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679663"
---
# <a name="lineopenoption_-constants"></a>\_Константы линеопеноптион

В **\_ константах линеопеноптион** перечислены доступные параметры для открытия строки.

<dl> <dt>

<span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**\_прокси-сервер линеопеноптион**
</dt> <dd> <dl> <dt>



Приложение предназначено для обработки запросов от других приложений, в которых линия открыта.


</dt> </dl> </dd> <dt>

<span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**ЛИНЕОПЕНОПТИОН \_ синглеаддресс**
</dt> <dd> <dl> <dt>



Приложение должно информировать о новых вызовах, созданных на устройстве, только в том случае, если эти вызовы появляются по адресу, указанному в элементе **дваддрессид** в структуре [**линекаллпарамс**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) , на которую указывает параметр *лпкаллпарамс* .


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Дополнительные сведения о работе этих параметров см. в разделе [**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




