---
description: 'Константы РЕНДБИНД — это флаги, используемые методом Итдиректори:: BIND для обозначения типов предоставленной проверки подлинности.'
ms.assetid: 27bcf36a-1826-4603-9821-22fcc5c1e186
title: Константы RENDBIND_ (rend. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badd2a48b2ae0632e317522533c664d4f74a6c77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689119"
---
# <a name="rendbind_-constants"></a>\_Константы рендбинд

\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Константы РЕНДБИНД — это флаги, используемые методом [**итдиректори:: BIND**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) для обозначения типов предоставленной проверки подлинности.

<dl> <dt>

<span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**\_Проверка подлинности рендбинд**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



Проверка подлинности пользователя.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**РЕНДБИНД \_ дефаултдомаиннаме**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



Использовать доменное имя по умолчанию.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**РЕНДБИНД \_ дефаултусернаме**
</dt> <dd> <dl> <dt>

 0x00000004
</dt> <dt>



Использовать имя пользователя по умолчанию.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**РЕНДБИНД \_ DEFAULTPASSWORD**
</dt> <dd> <dl> <dt>

 0x00000008
</dt> <dt>



Использовать пароль по умолчанию.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**РЕНДБИНД \_ дефаулткредентиалс**
</dt> <dd> <dl> <dt>

 0x0000000e
</dt> <dt>



Предыдущие три ORed вместе для удобства.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>Rend. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итдиректори**](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[**Итдиректори:: BIND**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind)
</dt> </dl>

 

 




