Interfaces
==========

Model Interfaces
----------------

.. _component_promotion_model_promotion-subject-interface:

PromotionSubjectInterface
~~~~~~~~~~~~~~~~~~~~~~~~~

To characterize an object with attributes and options from a promotion, the object class needs to implement
the **PromotionSubjectInterface**.

.. note::

    You will find more information about this interface in `Sylius API PromotionSubjectInterface`_.

.. _Sylius API PromotionSubjectInterface: http://api.sylius.org/Sylius/Component/Promotion/Model/PromotionSubjectInterface.html

.. _component_promotion_model_promotion-interface:

PromotionInterface
~~~~~~~~~~~~~~~~~~

This interface should be implemented by models representing a **Promotion**.

.. note::

    This interface extends the :ref:`component_resource_model_code-aware-interface` and :ref:`component_resource_model_timestampable-interface`.

    You will find more information about this interface in `Sylius API PromotionInterface`_.

.. _Sylius API PromotionInterface: http://api.sylius.org/Sylius/Component/Promotion/Model/PromotionInterface.html

.. _component_promotion_model_action-interface:

ActionInterface
~~~~~~~~~~~~~~~

This interface should be implemented by models representing an **Action**.

An **ActionInterface** has two defined types by default:

+--------------------------+---------------------+
| Related constant         | Type                |
+==========================+=====================+
| TYPE_FIXED_DISCOUNT      | fixed_discount      |
+--------------------------+---------------------+
| TYPE_PERCENTAGE_DISCOUNT | percentage_discount |
+--------------------------+---------------------+

.. note::

    You will find more information about this interface in `Sylius API ActionInterface`_.

.. _Sylius API ActionInterface: http://api.sylius.org/Sylius/Component/Promotion/Model/ActionInterface.html

.. _component_promotion_model_coupon-interface:

CouponInterface
~~~~~~~~~~~~~~~

This interface should be implemented by models representing a **Coupon**.

.. note::

    This interface extends the :ref:`component_resource_model_code-aware-interface`
    and the :ref:`component_resource_model_timestampable-interface`.

    You will find more information about this interface in `Sylius API CouponInterface`_.

.. _Sylius API CouponInterface: http://api.sylius.org/Sylius/Component/Promotion/Model/CouponInterface.html

.. _component_promotion_model_rule-interface:

RuleInterface
~~~~~~~~~~~~~

This interface should be implemented by models representing a **Rule**.

A **RuleInterface** has two defined types by default:

+-----------------------+------------+
| Related constant      | Type       |
+=======================+============+
| TYPE_ITEM_TOTAL       | item_total |
+-----------------------+------------+
| TYPE_ITEM_COUNT       | item_count |
+-----------------------+------------+

.. note::

    You will find more information about this interface in `Sylius API RuleInterface`_.

.. _Sylius API RuleInterface: http://api.sylius.org/Sylius/Component/Promotion/Model/RuleInterface.html

.. _component_promotion_model_promotion-countable-subject-interface:

PromotionCountableSubjectInterface
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To be able to count the object's promotion subjects, the object class needs to implement
the ``PromotionCountableSubjectInterface``.

.. note::

    This interface extends the :ref:`component_promotion_model_promotion-subject-interface`.

    You will find more information about this interface in `Sylius API PromotionCountableSubjectInterface`_.

.. _Sylius API PromotionCountableSubjectInterface: http://api.sylius.org/Sylius/Component/Promotion/Model/PromotionCountableSubjectInterface.html

.. _component_promotion_model_promotion-coupon-aware-subject-interface:

PromotionCouponAwareSubjectInterface
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To make the object able to get its associated coupon, the object class needs to implement
the ``PromotionCouponAwareSubjectInterface``.

.. note::

    This interface extends the :ref:`component_promotion_model_promotion-subject-interface`.

    You will find more information about this interface in `Sylius API PromotionCouponAwareSubjectInterface`_.

.. _Sylius API PromotionCouponAwareSubjectInterface: http://api.sylius.org/Sylius/Component/Promotion/Model/PromotionCouponAwareSubjectInterface.html

.. _component_promotion_model_promotion-coupons-aware-subject-interface:

PromotionCouponsAwareSubjectInterface
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To make the object able to get its associated coupons collection, the object class needs to implement
the ``PromotionCouponsAwareSubjectInterface``.

.. note::

    This interface extends the :ref:`component_promotion_model_promotion-subject-interface`.

    You will find more information about this interface in `Sylius API PromotionCouponsAwareSubjectInterface`_.

.. _Sylius API PromotionCouponsAwareSubjectInterface: http://api.sylius.org/Sylius/Component/Promotion/Model/PromotionCouponsAwareSubjectInterface.html


Services Interfaces
-------------------

.. _component_promotion_checker_promotion-eligibility-checker-interface:

PromotionEligibilityCheckerInterface
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Services responsible for checking the promotions eligibility on the promotion subjects should implement this interface.

.. note::

    You will find more information about this interface in `Sylius API PromotionEligibilityCheckerInterface`_.

.. _Sylius API PromotionEligibilityCheckerInterface: http://api.sylius.org/Sylius/Component/Promotion/Checker/PromotionEligibilityCheckerInterface.html

.. _component_promotion_checker_promotion-rule-checker-interface:

RuleCheckerInterface
~~~~~~~~~~~~~~~~~~~~

Services responsible for checking the rules eligibility should implement this interface.

.. note::

    You will find more information about this interface in `Sylius API RuleCheckerInterface`_.

.. _Sylius API RuleCheckerInterface: http://api.sylius.org/Sylius/Component/Promotion/Checker/RuleCheckerInterface.html

.. _component_promotion_action_promotion-applicator-interface:

PromotionApplicatorInterface
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Service responsible for applying promotions in your system should implement this interface.

.. note::

    You will find more information about this interface in `Sylius API PromotionApplicatorInterface`_.

.. _Sylius API PromotionApplicatorInterface: http://api.sylius.org/Sylius/Component/Promotion/Action/PromotionApplicatorInterface.html

.. _component_promotion_processor_promotion-processor-interface:

PromotionProcessorInterface
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Service responsible for checking all rules and applying configured actions if rules are eligible in your system should implement this interface.

.. note::

    You will find more information about this interface in `Sylius API PromotionProcessorInterface`_.

.. _Sylius API PromotionProcessorInterface: http://api.sylius.org/Sylius/Component/Promotion/Processor/PromotionProcessorInterface.html

.. _component_promotion_repository_promotion-repository-interface:

PromotionRepositoryInterface
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In order to be able to find active promotions in your system you should create a repository class which implements this interface.

.. note::
    This interface extends the :ref:`component_resource_repository_repository-interface`.

    For more detailed information about this interface go to `Sylius API PromotionRepositoryInterface`_.

.. _Sylius API PromotionRepositoryInterface: http://api.sylius.org/Sylius/Component/Promotion/Repository/PromotionRepositoryInterface.html

.. _component_promotion_generator_coupon-generator-interface:

CouponGeneratorInterface
~~~~~~~~~~~~~~~~~~~~~~~~

In order to automate the process of coupon generation your system needs to have a service that will implement this interface.

.. note::

    For more detailed information about this interface go to `Sylius API CouponGeneratorInterface`_.

.. _Sylius API CouponGeneratorInterface: http://api.sylius.org/Sylius/Component/Promotion/Generator/CouponGeneratorInterface.html

.. _component_promotion_model_action-action-interface:

PromotionActionInterface
~~~~~~~~~~~~~~~~~~~~~~~~

This interface should be implemented by services that execute actions on the promotion subjects.

.. note::

    You will find more information about this interface in `Sylius API PromotionActionInterface`_.

.. _Sylius API PromotionActionInterface: http://api.sylius.org/Sylius/Component/Promotion/Action/PromotionActionInterface.html
