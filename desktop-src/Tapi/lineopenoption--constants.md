---
description: В \_ константах линеопеноптион перечислены доступные параметры для открытия строки.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: Константы LINEOPENOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0dc6a4780b366b2dce08110ecce40c7140ab1d0956d788dce5a67d5d0501b6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739254"
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

## <a name="remarks"></a>Remarks

Дополнительные сведения о работе этих параметров см. в разделе [**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Заголовок<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




